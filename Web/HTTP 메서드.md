# HTTP

웹상에서 클라이언트와 서버 간에 요청 및 응답으로 데이터를 주고받는 프로토콜이다. HTTP 메서드는 서버가 요청을 수행하기 위해 해야 할 행동을 표시하는 용도로 사용된다.

### HTTP 메서드

- GET
- POST
- PUT
- PATCH
- DELETE

# GET

리소스를 조회할 때 주로 사용한다. 서버에 전달하고 싶은 데이터는 query(쿼리 파라미터, 쿼리 스트링)를 통해 전달한다. 캐싱이 가능하지만, URL에 데이터가 노출되어 보안에 취약하다.

# POST

메세지 바디를 통해 서버로 요청 데이터 전달한다. 따라서 대용량 데이터도 전송이 가능하다. 데이터가 바디로 전송되어 안전하다고 보일 수 있지만, 크롬 개발자 도구나 Fiddler와 같은 툴로 내용을 확인할 수 있기 때문에 암호화가 필요하다. 캐싱이 불가능하다.

# GET과 POST의 차이, 멱등의 유무

멱등(idempotent)의 법칙이란 똑같은 연산을 수행했을 때 같은 결과가 나오는 연산을 가리키는 수학 용어이다.  
GET 방식은 멱등이 적용된다. 서버에게 동일한 요청을 전송하더라도 동일한 응답이 돌아온다. 하지만 POST 방식은 서버에게 동일한 요청을 전송하더라도 응답은 항상 다를 수 있다. 따라서 멱등이 적용되지 않는다.

# PUT

리소스를 대체한다. 리소스가 있으면 대체하고, 없으면 생성한다. 멱등이 적용된다.

# PATCH

리소스를 부분 변경한다. PATCH가 지원이 안 될 경우, POST로 사용 가능하다. 캐싱이 불가능하다.

# DELETE

리소스를 제거한다. 멱등이 적용된다.

# 참고

> [https://sseambong.tistory.com/5](https://sseambong.tistory.com/5)  
> [https://mangkyu.tistory.com/17](https://mangkyu.tistory.com/17)  
> [https://noahlogs.tistory.com/35](https://noahlogs.tistory.com/35)  
> [https://hongsii.github.io/2017/08/02/what-is-the-difference-get-and-post/](https://hongsii.github.io/2017/08/02/what-is-the-difference-get-and-post/)  
> [http://blog.naver.com/PostView.nhn?blogId=kdmerit&logNo=220581326136](http://blog.naver.com/PostView.nhn?blogId=kdmerit&logNo=220581326136)
