# HTTP(HyperText Transfer Protocol)

웹 페이지 문서를 웹 서버에 전송 요청하는 프로토콜이다. 비연결형 서비스이며, 특정 부분에서 접속이 끊어졌을 경우 다시 시작할 필요가 없다.

# HTTPS(HyperText Transfer Protocol over Secure Socket Layer)

보안이 강화된 HTTP이며, 내가 사이트에 보내는 정보를 제 3자가 못 보게 한다. 내가 접속한 사이트가 믿을만한 곳인지 알려준다.

### 문제점

- 암호화 작업을 거쳐야 하므로, 웹 서버에 부하가 생긴다.
- 접속이 끊어졌을 경우 인증이 필요하므로 재접속 과정에서 과부하 문제가 발생한다.
- 서버 보안 인증서를 구매해야 한다.

# 로그인 과정

예를 들어, 특정 홈페이지에 아이디와 비밀번호를 작성하고 로그인을 누르면 이러한 정보는 인터넷을 타고 홈페이지의 서버로 전송된다. 그런데 그냥 HTTP로 보낸다면 이 정보는 입력한 텍스트 그대로 보내진다. 누구든 알아볼 수 있는 형식이기 때문에 개인 정보를 침해할 수 있다. 그런데 HTTPS는 이러한 개인 정보를 해당 홈페이지만 알아볼 수 있는 암호화된 텍스트로 변경해서 서버로 전송된다. 이 방식은 다른 누군가로부터 정보를 보호할 수 있다.

# SSL과 TLS

1. 네스케이프에 의해서 SSL이 발명하였다.
2. 이것이 점차 폭넓게 사용되다가 표준화 기구인 IETF의 관리로 변경되면서 TLS라는 이름으로 변경되었다.
3. 하지만 TLS라는 이름보다 SSL이라는 이름을 훨씬 많이 사용하고 있다.

HTTPS는 SSL 프로토콜 위에서 돌아가는 프로토콜이다. SSL은 암호화된 데이터를 전송하기 위해서 공개키와 대칭키를 혼합해서 사용한다.

### 대칭키

하나의 키로 데이터를 암호화하고 복호화 한다. 암복호화에 드는 비용이 적지만, 하나의 키로 암복호화를 하기 때문에 해당 키가 노출된다면 보안상 치명적인 문제가 발생한다.

### 공개키

2개의 키(공개키,비공개키)로 암호화하고 복호화 한다. 공개키로 데이터를 암호화하면 반드시 비공개키로만 복호화 가능하고 비공개키로 데이터를 암호화하면 공개키로만 복호화 할 수 있다. 비공개키는 자신만이 가지고 있고, 공개키는 타인에게 제공한다.

# 결론

모든 웹페이지에서 HTTPS를 사용하지 않는다. 평문 통신에 비해서 암호화 통신은 CPU나 메모리 등 리소스를 많이 필요로 하기 때문이다. 통신할 때마다 암호화를 하면 리소스를 소비하기 때문에 서버 한 대당 처리할 수 있는 Request 수가 줄어들게 된다. HTTPS라 하여 무조건 안전한 것은 아니고, 웹 브라우저에서의 구현 정확도와 서버 소프트웨어, 지원하는 암호화 알고리즘에 따라 보안 수준이 다르다. 따라서 **민감한 정보를 다룰 때**만 **HTTPS에 의한 암호화 통신을 사용**해야 한다.

# 참고

> [https://devdy.tistory.com/14](https://devdy.tistory.com/14)  
> [https://coding-start.tistory.com/208](https://coding-start.tistory.com/208)  
> [https://opentutorials.org/course/228/4894](https://opentutorials.org/course/228/4894)  
> [https://github.com/WooVictory/Ready-For-Tech-Interview/blob/master/Network/HTTP%2C%20HTTPS.md](https://github.com/WooVictory/Ready-For-Tech-Interview/blob/master/Network/HTTP%2C%20HTTPS.md)  
> [https://youtu.be/Ar61pammhog](https://youtu.be/Ar61pammhog)  
> [https://youtu.be/H6lpFRpyl14](https://youtu.be/H6lpFRpyl14)
