# ๐ HTTP(HyperText Transfer Protocol)

## ๋ชฉ์ฐจ
- [HTTP ์ ์](#HTTP-์ ์)
- [HTTP ๋์](#HTTP-๋์)
- [๋ชจ๋ ๊ฒ์ด HTTP](#๋ชจ๋ ๊ฒ์ด-HTTP)
- [HTTP ํ์ ๋ฐฐ๊ฒฝ](#HTTP-ํ์-๋ฐฐ๊ฒฝ)
- [HTTP ์ญ์ฌ](#HTTP-์ญ์ฌ)
- [HTTP ํน์ง](#HTTP-ํน์ง)


## HTTP ์ ์
- HTML๊ณผ ๊ฐ์ ํ์ดํผ๋ฏธ๋์ด ๋ฌธ์๋ฅผ ์ ์กํ๊ธฐ ์ํ ์ ํ๋ฆฌ์ผ์ด์ ๊ณ์ธต ํ๋กํ ์ฝ
- ํด๋ผ์ด์ธํธ์์ ์๋ฒ๊น์ง ์ผ๋ จ์ ํ๋ฆ์ ๊ฒฐ์ ํ๊ณ  ์๋ ๊ฒ์ด ์น์์ HTTP๋ผ๊ณ  ๋ถ๋ฆฌ๋ ํ๋กํ ์ฝ
    - ํ๋กํ ์ฝ: "์ฝ์", ์น์ HTTP๋ผ๋ ์ฝ์์ ์ฌ์ฉํ ํต์ ์ผ๋ก ์ด๋ฃจ์ด์ ธ์์
- ์ฆ, HTTP๋ **์ธํฐ๋ท์์ ๋ฐ์ดํฐ๋ฅผ ์ฃผ๊ณ ๋ฐ์ ์ ์๋ ํ๋กํ ์ฝ**

<br>

## HTTP ๋์
- ํด๋ผ์ด์ธํธ(์ฌ์ฉ์)๊ฐ ๋ธ๋ผ์ฐ์  ์ฃผ์ ์๋ ฅ๋์ URL์ ์๋ ฅํ์ฌ ์๋ฒ์๊ฒ **์์ฒญ(Request)** 
- ์๋ฒ๋ ํด๋ผ์ด์ธํธ์ ์์ฒญ์ ๋ง๋ ๊ฒฐ๊ณผ๋ฅผ ์ฐพ์์ ์ฌ์ฉ์์๊ฒ **์๋ต(Response)** ์ ํตํด ์นํ์ด์ง๊ฐ ํ๋ฉด์ ํ์๋จ

![image](https://user-images.githubusercontent.com/50076031/124417544-57086b80-dd94-11eb-9e92-7e189b6ce591.png)

<br>

## ๋ชจ๋ ๊ฒ์ด HTTP
- HTTP ๋ฉ์์ง์ ๋ชจ๋  ๊ฒ์ ์ ์ก
  - HTML, TEXT, IMAGE, ํ์ผ
  - JSON, XML(API)
- ๊ฑฐ์ ๋ชจ๋  ํํ์ ๋ฐ์ดํฐ ์ ์ก์ด ๊ฐ๋ฅ
- ์๋ฒ๊ฐ์ ๋ฐ์ดํฐ๋ฅผ ์ฃผ๊ณ  ๋ฐ์๋๋ ๋๋ถ๋ถ HTTP๋ฅผ ์ฌ์ฉ

<br>

## HTTP ํ์ ๋ฐฐ๊ฒฝ
- 1989๋ 3์, ํ ๋ฒ๋์ค ๋ฆฌ ๋ฐ์ฌ์ ์ํด ์ฒ์ ์ค๊ณ ๋จ
- ํ ๋ฒ๋์ค ๋ฆฌ ๋ฐ์ฌ๋, ๋ฉ๋ฆฌ ๋จ์ด์ ธ์๋ ๋๋ฃ ์ฐ๊ตฌ์์ ์ง์์ ๊ณต์ฉํ๊ฒ ํ  ์ ์๋๋ก ์์คํ์ ๊ณ ์
- ์ต์ด ๊ณ ์ํ ๊ฒ์ ์ฌ๋ฌ ๋ฌธ์๋ฅผ ์ํธ๊ฐ์ ๊ด๋ จ ์ง๋ ํ์ดํผํ์คํธ(HyperText)์ ์ํด ์ํธ๊ฐ์ ์ฐธ์กฐํ  ์ ์๋ 
  [WWW(World Wide Web)](https://en.wikipedia.org/wiki/World_Wide_Web) ์ ๊ธฐ๋ณธ ๊ฐ๋์ด ๋๋ ๊ฒ
- ์ด๋ฐ WWW๋ฅผ ๊ตฌ์ฑํ๋ ๊ธฐ์ ๋ก์ ๋ค์๊ณผ ๊ฐ์ ์ธ ๊ฐ์ง๊ฐ ์ ์๋จ
  - HTML(HyperText Markup Language): ๋ฌธ์ ๊ธฐ์  ์ธ์ด
  - HTTP(HyperText Transfer Protocol): ๋ฌธ์ ์ ์ก ํ๋กํ ์ฝ
  - URL(Uniform Resource Locator): ๋ฌธ์์ ์ฃผ์๋ฅผ ์ง์ ํ๋ ๋ฐฉ๋ฒ
- WWW๋ ์ง๊ธ์ผ๋ก ๋งํ์๋ฉด ์น ๋ธ๋ผ์ฐ์ , ๋จ์ํ ์น(Web)์ด๋ผ๊ณ  ๋ถ๋ฆผ

<br>

## HTTP ์ญ์ฌ

### HTTP/0.9 (1991๋)
- GET ๋ฉ์๋๋ง ์ง์
- HTTP ํค๋ X
- HTTP๊ฐ ์ ์ ์ฌ์์๋ ์๋์์

### HTTP/1.0 (1996๋)
- HTTP๊ฐ ์ ์ ์ฌ์์ผ๋ก ๊ณต๊ฐ
- ์ด๋, HTTP/1.0 ์ผ๋ก [RFC1945](https://blog.edit.kr/entry/%ED%8E%8CRFC-1945-Korean-EditionHTTP10-Korean-Version-30) ๊ฐ ๋ฐํ
- ์ด๊ธฐ ์ฌ์์ด์ง๋ง ํ์ฌ์๋ ์์ง ๋ง์ ์๋ฒ์์์ ํ์ญ์ผ๋ก ๊ฐ๋๋๊ณ  ์๋ ํ๋กํ ์ฝ ์ฌ์
- ๋ฉ์๋, HTTP ํค๋ ์ถ๊ฐ

```html
RFC(Request For Comments)
๊ตญ์  ์ธํฐ๋ท ํ์คํ ๊ธฐ๊ตฌ(IETF)์์ ์ธํฐ๋ท์์ ๊ธฐ์ ์ ๊ตฌํํ๋๋ฐ 
ํ์ํ ์์ธ ์ ์ฐจ์ ๊ธฐ๋ณธ ํ์ ์ ๊ณตํ๋ ๊ธฐ์  ๊ด๋ จ ๋ฌธ์๋ฅผ ์๋ฏธํจ
```

### **HTTP/1.1 (1997๋)**
- ํ์ฌ ์ธํฐ๋ท์์ ๊ฐ์ฅ ๋ง์ด ์ฌ์ฉ๋๋ ๋ฒ์ 
- RFC2068 (1997) -> RFC2616 (1999) -> RFC7230~7235 (2014) ๋ฑ์ ์์ผ๋ก ๋ฐํ

### HTTP/2 (2015๋)
- ์ฑ๋ฅ ๊ฐ์ 
- [what-is-http2](https://kinsta.com/learn/what-is-http2/)

### HTTP/3 (์งํ์ค)
- ์ฑ๋ฅ ๊ฐ์ 
- [TCP ๋์  UDP ์ฌ์ฉ](https://evan-moon.github.io/2019/10/08/what-is-http3/)

<br>

## HTTP ํน์ง
- ํด๋ผ์ด์ธํธ ์๋ฒ ๊ตฌ์กฐ
- ๋ฌด์ํ(Stateless) ํ๋กํ ์ฝ
- ๋น์ฐ๊ฒฐ์ฑ(Connectionless)
- ํด๋ผ์ด์ธํธ์ ์๋ฒ ๊ตฌ์กฐ์ HTTP ๋ฉ์์ง
- TCP/IP๋ฅผ ์ด์ฉํ๋ ์์ฉ ํ๋กํ ์ฝ

### ํด๋ผ์ด์ธํธ ์๋ฒ ๊ตฌ์กฐ
- Request(์์ฒญ), Response(์๋ต) ๊ตฌ์กฐ
- ํด๋ผ์ด์ธํธ๋ ์๋ฒ์ ์์ฒญ์ ๋ณด๋ด๊ณ , ์๋ต์ ๋๊ธฐ
- ์๋ฒ๋ ํด๋ผ์ด์ธํธ์ ์์ฒญ์ ๋ํ ๊ฒฐ๊ณผ๋ฅผ ๋ง๋ค์ด์ ์๋ต

![image](https://user-images.githubusercontent.com/50076031/124419440-70abb200-dd98-11eb-98fe-a3bdcfd3c34d.png)

### ๋ฌด์ํ(Stateless) ํ๋กํ ์ฝ
- ์๋ฒ๊ฐ ํด๋ผ์ด์ธํธ์ ์ํ๋ฅผ ๋ณด์กดํ์ง ์์
- ์ฅ์ : ์๋ฒ์ ํ์ฅ์ฑ์ด ๋์(Scale Out)
- ๋จ์ : ์ํ๋ฅผ ๋ณด์กดํ์ง ์๊ธฐ ๋๋ฌธ์ ํด๋ผ์ด์ธํธ๊ฐ ์ถ๊ฐ๋ก ๋ฐ์ดํฐ๋ฅผ ์ ์กํด์ผ ํจ
- ์ํ์ ์ง(Stateful)์ ๋ฌด์ํ(Stateless)์ ๊ฐ๋จ ์์

```html
๊ณ ๊ฐ(ํด๋ผ์ด์ธํธ), ์ ์(์๋ฒ)

** ์ํ์ ์ง - Stateful **
๊ณ ๊ฐ: ์ด ๋ธํธ๋ถ ์ผ๋ง?
์ ์: 100๋ง์
๊ณ ๊ฐ: 2๊ฐ ๊ตฌ๋งค
์ ์: 200๋ง์, ์ ์ฉ์นด๋ & ํ๊ธ ์ด๋ค๊ฑฐ๋ก ๊ตฌ๋งค?
๊ณ ๊ฐ: ์ ์ฉ์นด๋
์ ์: 200๋ง์ ๊ฒฐ์  ์๋ฃ

์ ์์ด ๊ณ ๊ฐ์ ๋ชจ๋  ์ํ(์ ๋ณด)๋ฅผ ์ ์งํ๊ณ  ์์ -> ๋ธํธ๋ถ, ๊ฐ๊ฒฉ
๋ฐ๋ผ์ ๊ณ ๊ฐ์ด ๋ชจ๋  ๋ฐ์ดํฐ๋ฅผ ์ ์กํ์ง ์๊ณ , ํ์ํ ๋ฐ์ดํฐ๋ฅผ ๊ทธ๋๊ทธ๋ ์ ์กํด๋
์ํ๋ฅผ ์ ์งํ๊ณ  ์๊ธฐ ๋๋ฌธ์ ์ ์์ ์๊ณ ์์


** ์ํ์ ์ง - Stateful(์ค๊ฐ์ ์ ์์ด ๋ฐ๋๋ฉด?) **
๊ณ ๊ฐ: ์ด ๋ธํธ๋ถ ์ผ๋ง?
์ ์A: 100๋ง์
๊ณ ๊ฐ: 2๊ฐ ๊ตฌ๋งค
์ ์B: ? ๋ฌด์์ 2๊ฐ ๊ตฌ๋งค?
๊ณ ๊ฐ: ์ ์ฉ์นด๋
์ ์C: ? ๋ฌด์์ ๋ช๊ฐ ์ ์ฉ์นด๋๋ก ๊ตฌ๋งค?



** ๋ฌด์ํ - Stateless **
๊ณ ๊ฐ: ์ด ๋ธํธ๋ถ ์ผ๋ง?
์ ์: 100๋ง์
๊ณ ๊ฐ: ๋ธํธ๋ถ 2๊ฐ ๊ตฌ๋งค
์ ์: ๋ธํธ๋ถ 2๊ฐ๋ 200๋ง์, ์ ์ฉ์นด๋ & ํ๊ธ ์ด๋ค๊ฑฐ๋ก ๊ตฌ๋งค?
๊ณ ๊ฐ: ๋ธํธ๋ถ 2๊ฐ ์ ์ฉ์นด๋๋ก ๊ตฌ๋งค
์ ์: 200๋ง์ ๊ฒฐ์  ์๋ฃ



** ๋ฌด์ํ - Stateless(์ ์์ด ์ค๊ฐ์ ๋ฐ๋๋ฉด?) **
๊ณ ๊ฐ: ์ด ๋ธํธ๋ถ ์ผ๋ง?
์ ์A: 100๋ง์
๊ณ ๊ฐ: ๋ธํธ๋ถ 2๊ฐ ๊ตฌ๋งค
์ ์B: ๋ธํธ๋ถ 2๊ฐ๋ 200๋ง์, ์ ์ฉ์นด๋ & ํ๊ธ ์ด๋ค๊ฑฐ๋ก ๊ตฌ๋งค?
๊ณ ๊ฐ: ๋ธํธ๋ถ 2๊ฐ ์ ์ฉ์นด๋๋ก ๊ตฌ๋งค
์ ์C: 200๋ง์ ๊ฒฐ์  ์๋ฃ



** ์ํ์ ์ง, ๋ฌด์ํ ์ฐจ์ด **
- ์ํ์ ์ง(Stateful): ์ค๊ฐ์ ๋ค๋ฅธ ์ ์์ผ๋ก ๋ฐ๋๋ฉด ์ด์ ์ ์ ๋ณด๋ฅผ ๋ชจ๋ฅด๊ธฐ ๋๋ฌธ์ ์๋จ
- ๋ฌด์ํ(Stateless): ์ค๊ฐ์ ๋ค๋ฅธ ์ ์์ผ๋ก ๋ฐ๋์ด๋ ๋จ
  -> ๊ฐ์๊ธฐ ๊ณ ๊ฐ์ด ์ฆ๊ฐํด๋ ์ ์์ ๋๊ฑฐ ํฌ์์ด ๊ฐ๋ฅ
  -> ๊ฐ์๊ธฐ ํด๋ผ์ด์ธํธ์ ์์ฒญ(ํธ๋ํฝ)์ด ์ฆ๊ฐํด๋ ์๋ฒ๋ฅผ ๋๊ฑฐ ํฌ์(์ค์ผ์ผ์์)์ด ๊ฐ๋ฅ

```

### ๋น์ฐ๊ฒฐ์ฑ(Connectionless)
- HTTP๋ ๊ธฐ๋ณธ์ ์ผ๋ก ์ฐ๊ฒฐ์ ์ ์งํ์ง ์๋ ๋ชจ๋ธ
- ์ผ๋ฐ์ ์ผ๋ก ์ด ๋จ์ ์ดํ์ ๋น ๋ฅธ ์๋๋ก ์๋ต
- ์๋ฒ ์์์ ํจ์จ์ ์ผ๋ก ์ฌ์ฉํ  ์ ์์

์ฐ๊ฒฐ์ ์ ์งํ๋ ๋ชจ๋ธ

![image](https://user-images.githubusercontent.com/50076031/124420922-6ccd5f00-dd9b-11eb-9474-5d06041be445.png)

์ฐ๊ฒฐ์ ์ ์งํ์ง ์๋ ๋ชจ๋ธ

![image](https://user-images.githubusercontent.com/50076031/124420984-866ea680-dd9b-11eb-8f03-d99ea6b2a0dd.png)

#### ๋น์ฐ๊ฒฐ์ฑ์ ํ๊ณ์ ๊ทน๋ณต
- ํด๋ผ์ด์ธํธ์ ์์ฒญ์ ๋ฐ๋ผ TCP/IP ์ฐ๊ฒฐ์ ์๋ก ๋งบ์ด์ผ ํจ
  - [TCP/IP 3-way Handshake](https://github.com/JuHyun419/study/blob/master/computer-science/TCP-%EC%97%B0%EA%B2%B0%EC%84%A4%EC%A0%95%26%ED%95%B4%EC%A0%9C.md) ์๊ฐ ์ถ๊ฐ
  - ์น ๋ธ๋ผ์ฐ์ ๋ก ์ฌ์ดํธ๋ฅผ ์์ฒญํ๋ฉด HTML, CSS, JS, ์ด๋ฏธ์ง ๋ฑ ์๋ง์ ์์์ด ํจ๊ป ๋ค์ด๋ก๋ ๋์ด ๋นํจ์จ
  - ์ง๊ธ์ **HTTP ์ง์ ์ฐ๊ฒฐ(Persistent Connections)** ๋ก ๋ฌธ์  ํด๊ฒฐ
    - [`Keep Alive ๊ธฐ๋ฅ`](https://goodgid.github.io/HTTP-Keep-Alive/)
  - HTTP/2, HTTP/3์์ ๋ ๋ง์ ์ต์ ํ
  
HTTP ์ด๊ธฐ - ์ฐ๊ฒฐ & ์ข๋ฃ ๋ญ๋น

![image](https://user-images.githubusercontent.com/50076031/124421201-e1a09900-dd9b-11eb-9f41-089d8f09ce5e.png)

[HTTP ์ง์ ์ฐ๊ฒฐ(Persistent Connections)](https://brunch.co.kr/@sangjinkang/4)

![image](https://user-images.githubusercontent.com/50076031/124421205-e5ccb680-dd9b-11eb-8013-e98ba34ca537.png)

<br><br>

### References
  - https://developer.mozilla.org/en-US/docs/Web/HTTP
  - https://www.inflearn.com/course/http-%EC%9B%B9-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC/dashboard
  - http://www.yes24.com/Product/Goods/15894097Z
  - https://ahndrenaline.tistory.com/entry/RFC-%EB%AC%B8%EC%84%9C-1
