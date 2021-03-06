# π HTTP(HyperText Transfer Protocol)
[`HTTP`](https://github.com/JuHyun419/study/blob/master/computer-science/HTTP.md)

[`HTTP(2)`](https://github.com/JuHyun419/study/blob/master/computer-science/HTTP(2).md)


## [HTTP Header](https://developer.mozilla.org/ko/docs/Web/HTTP/Headers)
- HTTP μ μ‘μ νμν λͺ¨λ  λΆκ°μ λ³΄
    - ex) λ©μμ§ λ°λμ λ΄μ©, ν¬κΈ°, μμΆ, μΈμ¦, μλ²μ λ³΄, μΊμ λ±λ±

```html
ν€λ νλ λͺ: νλ κ°

== Request ==
GET /search?q=juhyun&hl=ko HTTP/1.1
<!-- Host: νλ λͺ, www.google.com: νλ κ° -->
Host: www.google.com 


== Response ==
HTTP/1.1 200 OK
Content-Type: text/html;charset=UTF-8 // HTTP ν€λ
Content-Length: 3423 // HTTP ν€λ
<html>
<body>...</body>
</html>
```

### 4μ’λ₯μ HTTP ν€λ νλ
- HTTP ν€λ νλλ μ©λμ λ°λΌ 4μ’λ₯λ‘ λΆλ₯λ¨

#### [μΌλ°μ  ν€λ νλ(General Header Fields)](https://developer.mozilla.org/ko/docs/Glossary/General_header)
- λ¦¬νμ€νΈ λ©μμ§μ λ¦¬μ€ν°μ€ λ©μμ§ λ λ€ μ¬μ©λλ ν€λ

#### [λ¦¬νμ€νΈ ν€λ νλ(Request Header Fields)](https://developer.mozilla.org/ko/docs/Glossary/Request_header)
- ν΄λΌμ΄μΈνΈμμ μλ²λ‘ μ‘μ λ λ¦¬νμ€νΈ λ©μμ§μ μ¬μ©λλ ν€λ
- λ¦¬νμ€νΈμ λΆκ°μ  μ λ³΄, ν΄λΌμ΄μΈνΈ μ λ³΄, λ¦¬μ€ν°μ€μ μ½νμΈ μ κ΄ν μ°μ  μμ λ±μ λΆκ°

#### [λ¦¬μ€ν°μ€ ν€λ νλ(Response Header Fields)](https://developer.mozilla.org/ko/docs/Glossary/Response_header)
- μλ²μμ ν΄λΌμ΄μΈνΈλ‘ μ‘μ ν λ¦¬μ€ν°μ€ λ©μμ§μ μ¬μ©λλ ν€λ
- λ¦¬μ€ν°μ€μ μ λ³΄μ μλ²μ μ λ³΄, ν΄λΌμ΄μΈνΈμ μΆκ° μ λ³΄ μκ΅¬ λ±μ λΆκ°ν¨

#### [μν°ν° ν€λ νλ(Entity Header Fields)](https://developer.mozilla.org/ko/docs/Glossary/Entity_header)
- λ¦¬νμ€νΈ λ©μμ§μ λ¦¬μ€ν°μ€ λ©μμ§μ ν¬ν¨λ μν°ν°μ μ¬μ©λλ ν€λ
- μ½νμΈ  κ°±μ  μκ° λ±μ μν°ν°μ κ΄ν μ λ³΄λ₯Ό λΆκ°

<br>

### HTTP/1.1 ν€λ νλ(RFC 2616)

#### μΌλ°μ  ν€λ νλ(General Header Fields)
|ν€λ νλ λͺ|μ€λͺ|
|----|-------------|
|[Cache-Control](https://developer.mozilla.org/ko/docs/Web/HTTP/Headers/Cache-Control)|μΊμ± λμ μ§μ |
|Connection|Hop-by-hop ν€λ, μ»€λ₯μ κ΄λ¦¬|
|Date|λ©μμ§ μμ± λ μ§|
|Pragma|λ©μμ§ μ μ΄|
|Trailer|λ©μμ§μ λμ μλ ν€λμ μλ|
|Transfer-Encoding|λ©μμ§ λ°λμ μ μ‘ μ½λ© νμ μ§μ |
|Upgrade|λ€λ₯Έ νλ‘ν μ½μ μκ·Έλ μ΄λ|
|Via|νλ‘μ μλ²μ κ΄ν μ λ³΄|
|Warning|μλ¬ ν΅μ§|

<br>

#### λ¦¬νμ€νΈ ν€λ νλ(Request Header Fields)
|ν€λ νλ λͺ|μ€λͺ|
|----|-------------|
|Accept|μ μ  μμ΄μ νΈκ° μ²λ¦¬ κ°λ₯ν λ―Έλμ΄ νμ|
|Accept-Charset|λ¬Έμμ μ°μ  μμ|
|Accept-Encoding|μ½νμΈ  μΈμ½λ© μ°μ  μμ|
|Accept-Language|μΈμ΄(μμ°μ΄) μ°μ  μμ|
|Authorization|μΉ μΈμ¦μ μν μ λ³΄|
|Expect|μλ²μ λν νΉμ  λμμ κΈ°λ|
|From|μ μ μ λ©μΌ μ£Όμ|
|Host|μκ΅¬λ λ¦¬μμ€μ νΈμ€νΈ|
|If-Match|μν°ν° νκ·Έμ λΉκ΅(μΊμ±)|
|If-None-Match|μν°ν° νκ·Έμ λΉκ΅(If-Match λ°λ, μΊμ±)|
|If-Modified-Since|λ¦¬μμ€μ κ°±μ  μκ° λΉκ΅(μΊμ±)|
|If-Unmodified-Since|λ¦¬μμ€μ κ°±μ  μκ° λΉκ΅(If-Modified-Since λ°λ, μΊμ±)|
|If-Range|λ¦¬μμ€κ° κ°±μ λμ§ μμ κ²½μ° μν°ν° λ°μ΄νΈ λ²μμ μκ΅¬λ₯Ό μ‘μ |
|Max-Forwards|μ΅λ μ μ‘ ν μ|
|Range|μν°ν° λ°μ΄νΈ λ²μ μκ΅¬|
|[Referer](https://developer.mozilla.org/ko/docs/Web/HTTP/Headers/Referer)|νμ¬ μμ²­λ νμ΄μ§μ λ§ν¬ μ΄μ μ μΉ νμ΄μ§ μ£Όμ<br>ex) Referer: https://developer.mozilla.org/en-US/docs/Web/JavaScript|
|TE|μ μ‘ μΈμ½λ©μ μ°μ  μμ|
|User-Agent|HTTP ν΄λΌμ΄μΈνΈμ μ λ³΄|

<br>

#### λ¦¬μ€ν°μ€ ν€λ νλ(Response Header Fields)
|ν€λ νλ λͺ|μ€λͺ|
|----|-------------|
|Accept-Ranges|λ°μ΄νΈ λ¨μμ μκ΅¬λ₯Ό μμ ν  μ μλμ§ μλμ§ μ¬λΆ|
|Age|λ¦¬μμ€μ μ§μ  κ²½κ³Ό μκ°|
|[ETag](https://developer.mozilla.org/ko/docs/Web/HTTP/Headers/ETag)|λ¦¬μμ€μ λ²μ μ μλ³νλ κ³ μ ν λ¬Έμμ΄ κ²μ¬κΈ°|
|[Location](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Location)|νμ΄μ§λ₯Ό λ¦¬λ€μ΄λ μν  URLμ λνλ|
|Proxy-Authenticate|νλ‘μ μλ²μ ν΄λΌμ΄μΈνΈ μΈμ¦μ μν μ λ³΄|
|Retry-After|λ¦¬νμ€νΈ μ¬μνμ νμ΄λ° μκ΅¬|
|Server|HTTP μλ² μ λ³΄|
|Vary|νλ‘μ μλ²μ λν μΊμ κ΄λ¦¬ μ λ³΄|
|WWW-Authenticate|μλ²μ ν΄λΌμ΄μΈνΈ μΈμ¦μ μν μ λ³΄|

<br>

#### μν°ν° ν€λ νλ(Entity Header Fields)
|ν€λ νλ λͺ|μ€λͺ|
|----|-------------|
|Allow|λ¦¬μμ€κ° μ κ³΅νλ HTTP λ©μλ|
|Content-Encoding|μν°ν° λ°λμ μ μ©λλ μ½νμΈ  μΈμ½λ©|
|Content-Language|μν°ν°μ μμ°μ΄|
|Content-Length|μν°ν° λ°λμ μ¬μ΄μ¦(λ¨μ: λ°μ΄νΈ)|
|Content-Location|λ¦¬μμ€μ λμνλ λμ²΄ URI|
|Content-MD5|μν°ν° λ°λμ λ©μμ§ λ€μ΄μ μ€νΈ|
|Content-Range|μν°ν° λ°λμ λ²μ μμΉ|
|[Content-Type](https://developer.mozilla.org/ko/docs/Web/HTTP/Headers/Content-Type)|μν°ν° λ°λμ λ―Έλμ΄ νμ|
|Expires|μν°ν° λ°λμ μ ν¨κΈ°κ° λ μ§|
|[Last-Modified](https://developer.mozilla.org/ko/docs/Web/HTTP/Headers/Last-Modified)|λ¦¬μμ€μ μ΅μ’ κ°±μ  λ μ§|

http://www.yes24.com/Product/Goods/15894097

![image](https://user-images.githubusercontent.com/50076031/127074085-95c5ef36-9d49-414d-b422-d87ace2aa949.png)


<br>

#### [μ½νμΈ  νμ](https://developer.mozilla.org/en-US/docs/Web/HTTP/Content_negotiation)
- ν΄λΌμ΄μΈνΈκ° μ νΈνλ νν μμ²­
- Accept: ν΄λΌμ΄μΈνΈκ° μ νΈνλ λ―Έλμ΄ νμ μ λ¬
- Accept-Charset: ν΄λΌμ΄μΈνΈκ° μ νΈνλ λ¬Έμ μΈμ½λ©
- Accept-Encoding: ν΄λΌμ΄μΈνΈκ° μ νΈνλ μμΆ μΈμ½λ©
- Accept-Language: ν΄λΌμ΄μΈνΈκ° μ νΈνλ μμ° μΈμ΄

- νμκ³Ό μ°μ μμ (1)
  - Quality Values(q)κ° μ¬μ©
  - 0 ~ 1, ν΄μλ‘ λμ μ°μ  μμ
  
- νμκ³Ό μ°μ μμ (2)
  - κ΅¬μ²΄μ μΈ κ²μ΄ μ°μ  μμ
- Googleμμ helloλ₯Ό κ²μνμ λ Network κ²°κ³Ό  

  <img width="630" alt="μΊ‘μ³ 22" src="https://user-images.githubusercontent.com/50076031/103978159-3208b680-51be-11eb-8079-63cc65eb8ec5.PNG">

<br>

#### [μΏ ν€(Cookie)](https://developer.mozilla.org/ko/docs/Web/HTTP/Headers/Cookie)
- [Set-Cookie](https://developer.mozilla.org/ko/docs/Web/HTTP/Headers/Set-Cookie): μλ²μμ ν΄λΌμ΄μΈνΈλ‘ μΏ ν€ μ λ¬(μλ΅)
- Cookie: ν΄λΌμ΄μΈνΈκ° μλ²λ‘λΆν° λ°μ μΏ ν€λ₯Ό μ μ₯νκ³  HTTP μμ²­μ μλ²λ‘ μ λ¬
  - μλͺμ£ΌκΈ°: Expires, max-age 
  
<br><br>

### References
- https://www.inflearn.com/course/http-%EC%9B%B9-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC#description
- http://www.yes24.com/Product/Goods/15894097
- https://developer.mozilla.org/ko/docs/Web/HTTP/Headers
