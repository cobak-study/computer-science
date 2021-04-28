# MVC 패턴(Model-View-Controller)

애플리케이션을 3가지 역할로 구분하여,
영역 간의 결합도를 최소화한 개발 방법론이다. MVC 패턴은 디자인 패턴 중 하나이다. 여기서 디자인 패턴은 SW 개발 방법을 공식화한 것을 의미한다.

## Model

Model은 컨트롤러가 호출할 때, 요청에 맞는 역할을 수행한다. 비즈니스 로직을 구현하는 영역으로 응용 프로그램에서 데이터를 처리한다. DB에 연결하고 데이터를 추출하거나 저장, 삭제, 업데이트, 변환 등의 작업을 수행한다.

## View

컨트롤러로부터 받은 모델의 결괏값을 가지고 사용자에게 출력할 화면을 제작한다. 화면에 표시되는 부분으로, 추출한 데이터나 일반적인 텍스트 데이터를 표시하거나 입력 폼 또는 사용자와의 상호작용을 위한 인터페이스를 표시하는 영역이다.

## Controller

일종의 조정자로, 클라이언트의 요청을 받았을 때 그 요청에 대해 실제 업무를 수행하는 모델 컴포넌트를 호출한다. 또한 클라이언트가 보낸 데이터가 있다면, 모델에 전달하기 쉽게 데이터를 가공한다. 모델이 작업을 마치면 그 결과를 뷰에게 전달한다.

# MVC 패턴의 흐름

![MVC 패턴의 흐름](https://mblogthumb-phinf.pstatic.net/MjAxNzAzMjVfMjUw/MDAxNDkwNDM4NzI4MTIy.4ZtITJJKJW_Nj1gKST0BhKMAzqmMaYIj9PobYJMFD4Ig.xTHT-0qyRKXsA4nZ2xKPNeCxeU2-tLIc-4oyrWq5WBgg.PNG.jhc9639/mvc_role_diagram.png?type=w800 "MVC 패턴의 흐름")

1. 사용자가 원하는 기능을 컨트롤러에 요청한다.
2. 요청을 받은 컨트롤러는 알맞은 모델에게 비즈니스 로직을 수행을 맡긴다.
3. 컨트롤러는 사용자에게 보여줄 뷰를 선택한다.
4. 선택된 뷰는 사용자에게 결과 화면을 보여준다. 이때 사용자에게 보여줄 데이터는 컨트롤러를 통해서 전달받는다.

# MVC 패턴의 장점

- 유연하고 확장하기 쉽다.
- 디자이너와 개발자의 협업이 용이하다.
- 유지 보수 비용 절감할 수 있다.

# MVC 패턴의 단점

- 기본 기능 설계를 위해 클래스들이 많이 필요하기 때문에 복잡하다.
- 설계 시간이 오래 걸리고 숙련된 개발자 필요하다.
- Model과 View의 완벽한 분리가 어렵다.

# 참고

> [https://asfirstalways.tistory.com/180](https://asfirstalways.tistory.com/180)  
> [https://m.blog.naver.com/jhc9639/220967034588](https://m.blog.naver.com/jhc9639/220967034588) > [https://youtu.be/uoVNJkyXX0I](https://youtu.be/uoVNJkyXX0I)  
> [https://server-engineer.tistory.com/167](https://server-engineer.tistory.com/167)  
> [https://wooaoe.tistory.com/15](https://wooaoe.tistory.com/15)
