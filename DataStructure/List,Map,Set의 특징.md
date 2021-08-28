# **List Map Set의 특징과 차이점**

## **📑 목차**

### **💻 [List](https://www.notion.so/7bcf78b1a08944a0864a9ffa03fa43b1)**

### **📌 [Map](https://www.notion.so/7bcf78b1a08944a0864a9ffa03fa43b1)**

### **✨ [Set](https://www.notion.so/7bcf78b1a08944a0864a9ffa03fa43b1)**

![https://user-images.githubusercontent.com/38427646/129674661-17003151-20ba-48ea-b3c1-95daadaa5a4c.png](https://user-images.githubusercontent.com/38427646/129674661-17003151-20ba-48ea-b3c1-95daadaa5a4c.png)

List, Queue, Tree 등 다양한 자료구조들이 있습니다.

이 중 면접 질문에 자주 나온다는 List, Set, Map에 대해 특징과 각각의 비교를 하겠습니다.

**배열**

- 크기 고정
- 삽입/삭제 시 오래걸린다는 단점이 있다.

이러한 단점들을 극복하고자 다양한 자료구조가 나오게 되었다.

### **List 무엇인가**

"리스트는 순서와 중복이 있는 자료구조"

![https://user-images.githubusercontent.com/38427646/129676208-f834ead2-e512-4c01-bf35-c38b89f2d7dc.png](https://user-images.githubusercontent.com/38427646/129676208-f834ead2-e512-4c01-bf35-c38b89f2d7dc.png)

**특징**

- 순서와 중복이 허용되는 자료구조
- List는 내부적으로 인덱스를 갖고 있을 수 있지만, elements 데이터는 다음 데이터는 이것이다~ 이렇게 데이터가 있는 순서가 있다는 것이 중요한 자료구조

**주요 기능**

- 처음, 끝, 중간에 엘리먼트를 추가/삭제하는 기능

  즉, 엘리먼트들이 리스트에 저장되어있을 때

  우리가 새로운 데이터를 처음, 중간, 끝에 추가/삭제를 할 수 있으며,

  그 과정에서 빈 공간이 생겼을 때에 하나씩 밀리면서 채운다.

- 리스트에 데이터가 있는지를 체크하는 기능

- 리스트의 모든 데이터에 접근할 수 있는 기능

**장점**

- 가변적인 배열, 배열이 자동으로 늘어남
- 비어있는 데이터가 없다.

**단점**

- 원하는 데이터가 뒤쪽에 위치하는 경우, 속도의 문제가 있을 수 있다.

  이유 : 순회를 하기 때문에

### **Map 무엇인가**

"키와 데이터를 같이 저장할 수 있는 자료구조"

**특징**

- Key, Value의 한 쌍으로 이루어진 데이터의 집합
- Key에는 중복된 값이 입력될 수 없다.
- 순서가 유지되지 않는다.
- Value의 중복은 허용된다.

**장점**

- 뛰어난 검색 속도를 갖고 있다.
- 인덱스가 따로 존재하지 않기 때문에 iterator를 사용합니다.

### **Set 무엇인가**

"순서없고 중복이 존재할 수 없는 자료구조"

**특징**

- 인덱스를 사용하지 않는다.
- 인덱스 매개변수가 없다.
- 집합에 빗대어 생각하면 좋을만한 자료구조

**장점**

- 빠른 검색 속도를 갖고 있다.
- 인덱스가 따로 존재하지 않기 때문에 iterator를 사용합니다.

Iterator는 자바 기준으로 hasNext(), next(), remove()함수를 사용하여 어떤 컬렉션이라도 동일한 방식으로 접근하여 그 항목들에 접근할 수 있는 방법을 제공하는 것 (자바의 특징 - 다형성)

**요약**

- List는 기본적으로 데이터들이 순서대로 저장되며 중복을 허용한다.
- Map은 순서가 보장되지 않고 Key값의 중복은 허용하지 않지만 Value값의 중복은 허용된다.
- Set은 순서가 보장되지 않고 데이터들의 중복을 허용하지 않는다.

수정해야할 부분이 있거나 보완해야하는 사항이 있다면 언제든지 말씀해주세요!

### **참고**

https://velog.io/@y1andyu/Data-Structure-1-자료구조란

https://milkoon1.tistory.com/44

https://www.youtube.com/watch?v=SLAl5MPAass

https://cocoon1787.tistory.com/527

https://modoocode.com/224