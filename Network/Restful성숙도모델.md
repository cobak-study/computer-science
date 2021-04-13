# Restful 성숙도모델

Date: Apr 13, 2021
공부함?: No

# Rest란 무엇이고 API란 무엇이고 RestAPI란 무엇일까?

API: 시스템간의 상호작용을 위한 인터페이스

REST API(RESTful API, 레스트풀 API)란 REST 아키텍처의 제약 조건을 준수하는 애플리케이션 프로그래밍 인터페이스를 뜻합니다. REST는 Representational State Transfer의 줄임말

HTTP URI(Uniform Resource Identifier)를 통해 자원(Resource)을 명시하고, HTTP Method(POST, GET, PUT, DELETE)를 통해 해당 자원에 대한 CRUD Operation을 적용하는 것을 의미한다.
[https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html](https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html)

# Restful 성숙도모델

레너드 리처드슨(Leonard Richardson)은 REST가 얼마나 성숙했는지 알 수 있는 아주 유용한 모델을 제시했습니다. 이 모델에 따르면 REST의 성숙도는 다음 4단계로 구분됩니다.

즉 높은 단계 일수록 "RestFul 스럽다" 라고 표현 할 수 있습니다.

- **레벨 0**: 단일 Endpoint를 사용하여 통신합니다.
단일 엔드포인트 이기 때문에, 매개변수를 통해 분기 처리를 합니다. 또한 이 매개변수를 Request Body로 활용하기 위해 HTTP method를 POST를 사용합니다.
그냥 POST 메소드만 사용하여 한 endpoint로 HTTP 통신으로 자원 요청하는 것 (graphql)

    ```cpp
    POST https://api/userService
    {
      "function": "getUserInfo",
      "arguments" [
        "1"
      ]
    }
    ```

    - 단일 Endpoint
    - 매개변수로 분기
    - HTTP method POST
- **레벨 1**: 서비스는 리소스 개념을 지원합니다.
리소스 도입, 리소스 별로 고유한 URI를 사용합니다. 즉 여러 엔드포인트를 사용합니다.
아직까지는 HTTP protocol을 전부 활용하고 있지 않으며, HTTP method는 GET, POST를 사용합니다.

    ```cpp
    POST https://api/userService
    {
      "function": "getUserInfo",
      "arguments" [
        "1"
      ]
    }

    GET https://api/userService/1
    ```

    - 리소스 도입
    - 여러 엔드포인트
    - HTTP method GET, POST
- **레벨 2**: 서비스는 HTTP 동사를 이용해서 액션을 수행하고(예: GET은 조회, POST는 생성, PUT은 수정), 요청 쿼리 매개변수 및 본문, 필요 시 매개변수를 지정합니다. 덕분에 서비스는 GET 요청을 캐싱하는 등 웹 인프라를 활용할 수 있습니다. ( GET 은 멱등성을 보장하고 있는 것임을 의미하며, 덕분에 클라이언트는 GET 요청에 의한 응답은 항상 같은 결과를 보장 받을 수 있다. )
또한 응답에 대해서는 알맞은 HTTP status code를 응답해야 합니다.

    ```cpp
    POST /api/users
    GET /api/users/1
    PUT /api/users/1
    DELETE /api/users/1
    ```

    - 리소스 행위에 대해 모든 HTTP method 사용
    - HTTP Cache 사용
    - HTTP status code 사용
- **레벨 3**: API 서비스의 모든 엔드포인트를 최초 진입점이 되는 URI를 통해 Hypertext Link 형태로 제공한다.
즉 API 목록 뿐만이 아니라, API 엔드포인트의 의존성까지 표현 할 수 있다. 이렇게 했을 때 클라이언트는 조금 더 유연하게 변경 될 URI도 알아챌 수 있게 된다.

    ```cpp
    GET https://api/

    HTTP/1.1 200 OK
    Content-Type: application/json
    {
      "/api/users",
      "/api/users/{userId}/roles",
      "/api/products",
      "/api/..."
    }
    ```

# 참고

> [https://ohjongsung.io/2018/07/21/rest-api-성숙도-모델-maturity-model](https://ohjongsung.io/2018/07/21/rest-api-%EC%84%B1%EC%88%99%EB%8F%84-%EB%AA%A8%EB%8D%B8-maturity-model)
[https://www.redhat.com/ko/topics/api/what-is-a-rest-api](https://www.redhat.com/ko/topics/api/what-is-a-rest-api)