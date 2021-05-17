# HTTP의 변화

![Untitled](https://user-images.githubusercontent.com/38197077/118433952-1a66af00-b717-11eb-80ec-34220a41522c.png)

# HTTP/0.9

HTTP 초기버전에는 버전 번호가 존재하지 않았습니다.

HTTP/0.9는 차후에 생길 버전들과 구별하기 위해 0.9로 명명되었습니다.

- GET Method만 존재
- 응답은 매우 간단한 형태
문서의 내용 본문 자체만을 그대로 돌려받는 식

    상태코드X 헤더X

    ```html
    <HTML>
    A very simple HTML page
    </HTML>
    ```

---

# HTTP/1.0

- 한 요청당 하나의 TCP 커넥션을 수립하고, 해당 요청의 응답이 이루어지면 연결된 TCP 커넥션을 끊는다.(**1요청당 1커넥션**)
- 상태코드가 응답의 시작 부분에 포함되기 시작 ( 이로 인해 요청에 대한 응답의 성공여부를 알 수 있게 되었습니다.)
- HTTP 헤더의 도입
    - 메타데이터 전송을 허용
    - 프로토콜을 유연하고 확장가능하도록 해줌
    - `Content-Type` 헤더로 인해 HTML 외의 다른 문서들도 전송 할 수 있게 되었음
    - 커넥션을 유지할 수 있게끔 하는 `keep-alive` 헤더

응답 예(일반적인 HTML 문서)

```html
GET /mypage.html HTTP/1.0
User-Agent: NCSA_Mosaic/2.0 (Windows 3.1)

200 OK
Date: Tue, 15 Nov 1994 08:12:31 GMT
Server: CERN/3.0 libwww/2.17
Content-Type: text/html
<HTML>
A page with an image
  <IMG SRC="/myimage.gif">
</HTML>
```

응답 예(gif 이미지 리소스)

```html
GET /myimage.gif HTTP/1.0
User-Agent: NCSA_Mosaic/2.0 (Windows 3.1)

200 OK
Date: Tue, 15 Nov 1994 08:12:32 GMT
Server: CERN/3.0 libwww/2.17
Content-Type: text/gif
(image content)
```

---

# HTTP/1.1

1999년 출시

- HTTP 1.0에서는 주로 Last-Modified, 즉 Dates에만 의존하여 caching이 이루어지지만, 1.1 버전부터는 client에서 사용 가능한 미디어 타입을 명시하여 지원한다.
- HTTP Persistent Connection 도입
지정한 시간동안 커넥션을 유지하도록 하는 개념
- HTTP pipelining 도입
다수의 요청이 일어나면, 여러 커넥션이 맺어지게 되는데, 이로 인해 브라우저는 각 요청들에 대한 응답을 순차적으로 기다려야 한다. 
``이 문제를 해결하기 위해 여러 요청과 응답을 순차적으로 처리하는 것이 아닌, 하나의 커넥션으로 다수의 요청과 응답을 처리할 수 있게 한 개념 ( 그럼에도 여전히 `Head Of Line Blocking` 문제를 가지고 있음, 왜? 파이프라이닝에서는 요청 된 순서대로 전체 요청을 반환해야 함 )

좌(http 1.0): 요청마다 새로운 connection을 수립

중간(http 1.1): keep-alive가 기본적으로 도입됌  커넥션 지속 ( `Connection: Keep-Alive` 헤더로 동작한다.)

우(http 1.1): connection pipelining 도입,  

![Untitled 1](https://user-images.githubusercontent.com/38197077/118433935-15a1fb00-b717-11eb-8041-65adb564e02f.png)

---

# HTTP/2.0

## HTTP1.1에서의 HOL문제해결

`Head Of Line Blocking`

![Untitled 2](https://user-images.githubusercontent.com/38197077/118433937-16d32800-b717-11eb-90a6-06a1fd73224b.png)

한 커넥션으로 여러 요청과 응답작업을 할 수 있지만, 결국 여러 응답중 처리시간이 가장 긴 처리시간이 지난 후에야 모든작업이 끝나게 된다.

![Untitled 3](https://user-images.githubusercontent.com/38197077/118433939-176bbe80-b717-11eb-8367-df9e52de7ab9.png)

HTTP/2에서는 HOL 문제를 해결하기 위해 Multiplexing 이라는 개념을 도입했고, Multiplexing은 동일한 TCP 연결을 통해 여러 요청을 전송하고 순서와 상관없이 응답을 수신하는 개념이다. 이로써 처리시간이 긴 응답이 다른 응답들의 처리시간을 블로킹하는 것을 방지한다.

- Multiplexing 도입으로 HOL 해결
- Header 정보를 압축, Header Table을 이용한 중복되는 헤더를 검출하여 중복제거

    ![Untitled 4](https://user-images.githubusercontent.com/38197077/118433941-18045500-b717-11eb-8a13-9727e0d65b93.png)

    - Server Push
    HTTP 통신은 단방향통신으로 클라이언트가 요청해야만 응답을 받을 수 있었다.
    Server Push는 이와는 반대로 클라이언트가 요청하지 않은 리소스를 전송할 수 있다.
    보통 HTML문서를 요청하게 되면 연관되어 있는 리소스(image, css, js)들을 다시 요청할 것이라는것을 예상 할 수 있는데, Server Push를 통해 사전에 연관된 리소스들을 클라이언트에서 다운로드 하도록 한다.

        ![Untitled 5](https://user-images.githubusercontent.com/38197077/118433942-18045500-b717-11eb-8034-a585a4f59aad.png)

    - Stream, Frame 도입
    HTTP1.1 에서는 메세지(Message)라는 단위로 데이터를 전송했지만,
    Stream과 Frame의 도입으로 좀 더 유연한 요청과 응답의 구조를 가지게 됐다.
    또한 이 구조 덕분에, 순서에 상관없이 비동기 방식으로 이루어지는 전송을 처리할 수 있게 되었다.
        - *스트림*: 구성된 연결 내에서 전달되는 바이트의 양방향 흐름이며, 하나 이상의 메시지를 포함한다.
        (각 스트림에는 양방향 메시지 전달에 사용되는 고유 식별자와 우선순위 정보(선택 사항)가 있다.)
        - *메시지*: 요청 또는 응답 메시지에 매핑되는 프레임의 전체 시퀀스
        - *프레임*: HTTP/2에서 통신의 최소 단위이며 각 최소 단위에는 하나의 프레임 헤더가 포함됩니다. 이 프레임 헤더는 최소한으로 프레임이 속하는 스트림을 식별합니다.

    ![Untitled 6](https://user-images.githubusercontent.com/38197077/118433944-189ceb80-b717-11eb-8f3a-8c84f338fd78.png))

    ![Untitled 7](https://user-images.githubusercontent.com/38197077/118433946-189ceb80-b717-11eb-95c6-341447cff3a0.png)

# 질문

1. 현재 기준 May 11, 2021 HTTP1.1 HTTP2.0보다 많이 사용되고 있을까?
HTTP 2.0은 [RFC 7540](https://datatracker.ietf.org/doc/html/rfc7540) 국제표준에 의해 공식 웹 표준 프로토콜로 지정되었다. (2015년 5월 14일)

    프로토콜 사용처에 따라 다른 것 같다

    ![Untitled 8](https://user-images.githubusercontent.com/38197077/118433947-19358200-b717-11eb-93a6-c21788f71470.png)

    HTTP 버전별 사용율 (요청)

    ![Untitled 9](https://user-images.githubusercontent.com/38197077/118433948-19ce1880-b717-11eb-90fd-82f8adb63669.png))

    HTTP 버전별 사용율 (홈페이지)

    ![Untitled 10](https://user-images.githubusercontent.com/38197077/118433951-19ce1880-b717-11eb-8443-3efbb15dafdd.png))

    HTTP 버전별 사용율 (암호화 프로토콜 HTTPS가 적용된 홈페이지)

2. HTTP2의 Multiplexing은 비동기 방식일까?
먼저 Multiplexing은 동일한 커넥션으로 한번에 여러 요청을 시작하여 순서에 상관없이 응답받을 수 있다는 것이 특징인데, 즉 async, non-block 방식을 사용하고 있다라고 해석해볼 수 있다. ( 요청마다의 응답을 즉시 완료되지 않더라도 리턴하고, 결과적으로 그 응답은 이벤트 핸들러(callback)에 의해 나중에 처리 )

# 참고

> [https://developer.mozilla.org/ko/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP](https://developer.mozilla.org/ko/docs/Web/HTTP/Basics_of_HTTP/Evolution_of_HTTP)
[https://medium.com/@sandeep4.verma/http-1-to-http-2-to-http-3-647e73df67a8](https://medium.com/@sandeep4.verma/http-1-to-http-2-to-http-3-647e73df67a8)
[https://www.slideshare.net/heavybit/heavybit-presents-ilya-grigorik-on](https://www.slideshare.net/heavybit/heavybit-presents-ilya-grigorik-on)
[https://livebook.manning.com/book/http2-in-action/chapter-7/](https://livebook.manning.com/book/http2-in-action/chapter-7/)
[https://almanac.httparchive.org/en/2019/http2#fig-4](https://almanac.httparchive.org/en/2019/http2#fig-4)
[https://stackoverflow.com/questions/36517829/what-does-multiplexing-mean-in-http-2/36519379](https://stackoverflow.com/questions/36517829/what-does-multiplexing-mean-in-http-2/36519379)