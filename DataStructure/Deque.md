# Deque (덱/데크)

## **📑 목차**

------

### ❓Deque 정의

### 💁🏻‍♀️ Deque 내장 함수

### **✨ 문제에 적용해보기**

------

우선,  이 블로그들을 보면서 **공부했던 내용을 정리한 글**이라는 점을 말씀드립니다! 🙂

[[자료구조\] 스택(Stack), 큐(Queue), 덱(Deque)](https://velog.io/@choiiis/자료구조-스택Stack과-큐Queue)

[[Java(자바)\] Deque(덱/데크) 자료구조](https://soft.plusblog.co.kr/24)

[Queue offer과 add의 차이](https://choijiuen.tistory.com/110)

[[JAVA\] Queue 관련 함수 (+ 함수 차이점)](https://conanglog.tistory.com/217)

https://lemonlemon.tistory.com/40

### ❓Deque 정의

![Deque](https://images.velog.io/images/esun1903/post/3f91d93c-ce79-4d20-9ce8-d7395b282af4/image.png)

- `Deque(Double Ended Queue)`, `queue`와 비슷하지만 `queue`는 `front`에서만 삭제하고, `end`에서 삽입하는데, `deque`는 `front`와 `end`에서 삭제와 삽입이 모두 가능하다.
- 연속적인 메모리를 기반으로 하는 '시퀀스 컨테이너'이다. 따라서, 임의 접근 반복자 제공.
- 여러 개의 메모리 단위로 데이터를 저장한다. vector는 메모리를 재할당하고 모든 요소를 복사하여야 하는데, deque는 새로운 메모리 단위를 할당하여 요소를 추가한다.또 데이터 요소를 저장하는 여러 개의 메모리 단위를 갖습니다.
- 크기가 가변적이다. (선언 후에 변경할 수 있다.)
- 중간 요소가 삽입, 삭제될 때, 요소들을 앞/뒤로 밀 수 있으므로 vector보다는 좋은 성능을 갖음. 그래도, 앞/뒤에서의 삽입/삭제 성능은 좋지만 중간에서는 좋지 않다.

### 시간 복잡도

삽입/삭제- 원소를 앞/뒤에 삽입하는 경우 : O(1)

원소를 앞/뒤에 삽입하는 경우 : O(1)

탐색- 원소를 탐색하는 경우 : O(1) (index 접근)

### 장점

데이터의 삽입과 삭제가 빠르다.

크기가 가변적이다.

앞, 뒤에서 데이터를 삽입/삭제할 수 있다.

index로 임의 원소 접근이 가능하다.

새로운 원소 삽입 시에, 메모리를 재할당하고 복사하지 않고 새로운 단위의 메모리 블록을 할당하여 삽입한다.

### 단점

deque의 중간에서의 삽입과 삭제가 어렵다.구현이 어렵다.

### 💁🏻‍♀️ Deque 내장 함수

**덱의 앞 부분에 값을 추가하기**

- addFirst()
- offerFirst()

**덱의 뒷 부분에 값을 추가하기**

- addLast()
- add()
- offerLast()
- offer()

여기서, add와 offer의 차이는 무엇일까요?

- add 메소드:  illegalStateException를 발생시킨다.
- offer 메서드 : 큐가 가득차서 더이상 추가할 수 없는 경우 false를 반환하고 요소가 추가되면 true를 반환하며 특정 예외를 throw하지 않는다.

**덱의 앞 부분에 값을 삭제하기**

- remove()
- removeFirst()
- pollFirst()
- poll()

**덱의 뒷 부분에 값을 삭제하기**

- removeLast()
- pollLast()

여기서, remove와 poll의 차이는 무엇일까요?

- remove 메소드 :  큐가 비어있을 때 삭제하면 예외 발생합니다.
- poll 메소드 : 큐가 비어있을 때 삭제하면 null을 반환합니다.

**덱의 앞 부분의 값을 가져오기 (읽기)**

- getFirst()
- peekFirst()
- peek()

**덱의 뒷 부분의 값을 가져오기 (읽기)**

- getLast()
- peekLast()

여기서, get과 peek의 차이는 무엇일까요?

- get 메소드 :  해당 값을 return 하고 실패 시 Exception을 발생시킵니다.
- peek 메소드 : 기본 적으로 해당 값을 반환한다는 점에서 get과 비슷하지만, 실패 시에 null을 return한다는 점이 차이점입니다.

### **✨ 문제에 적용해보기**

그럼, 여기서 deque를 사용하여 풀 수 있는 문제들을 보며 적용해보아요! 🙂

[3190번: 뱀](https://www.acmicpc.net/problem/3190)

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Deque;
import java.util.LinkedList;
import java.util.Queue;
import java.util.StringTokenizer;

public class Main {

	public static int N, L, K;
	public static int time = 0;

	public static Deque<Snake> deque = new LinkedList<>();
	public static Deque<Dir> direction = new LinkedList<>();

	public static void main(String[] args) throws IOException {

		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		StringTokenizer st;

		N = Integer.parseInt(br.readLine());
		int board[][] = new int[N + 1][N + 1];

		K = Integer.parseInt(br.readLine());
		for (int i = 0; i < K; i++) {
			st = new StringTokenizer(br.readLine());
			int r = Integer.parseInt(st.nextToken());
			int c = Integer.parseInt(st.nextToken());
			board[r-1][c-1] = 2; // 사과의 위치
		}

		L = Integer.parseInt(br.readLine());
		// 뱀의 방향 변환 정보
		for (int i = 0; i < L; i++) {
			st = new StringTokenizer(br.readLine());
			int time = Integer.parseInt(st.nextToken());
			String dir = st.nextToken();
			direction.add(new Dir(time, dir.charAt(0)));
		}

		gameStart(direction, board);
		System.out.println(time);

	}// end of main

	private static void gameStart(Queue<Dir> direction, int[][] board) {
		deque.addFirst(new Snake(0, 0, 1));
		board[0][0] = 1;

		// 머리 방향대로 기어가야함
		while (true) {
			Snake snake = deque.getFirst();
 
			int r = snake.r;
			int c = snake.c;
			int dir = snake.dir;
			// 1,1꺼냈어
			if (dir == 1) { // 방향이 오른쪽일때,
				c += 1;
			} else if (dir == 2) { // 2이면 위쪽
				r -= 1;
			} else if (dir == 3) { // 3이면 왼쪽
				c -= 1;
			} else if (dir == 4) { // 4이면 아래쪽
				r += 1;
			}
			time++;
			if (wallChecking(r, c) == true && board[r][c] != 1) {
				// 사과가 없을 때,
				if (board[r][c] != 2) {
					Snake tail = deque.pollLast();
					board[tail.r][tail.c] = 0;
				}

				deque.addFirst(new Snake(r, c, dir));
				dirChecking(time);
				board[r][c] = 1;
			} else {
				break;
			}

		}

	}// end of gameStart

	private static void dirChecking(int time) {

		if(direction.size()>0) {
		Dir d = direction.peekFirst();
		if (time == d.time) {
			Snake s = deque.getFirst();
			if (d.dir == 'L') {
				if (s.dir != 4) {
					s.dir += 1;
				} else {
					s.dir = 1;
				}
			} else {
				if (s.dir != 1) {
					s.dir -= 1;
				} else {
					s.dir = 4;
				}
			}
			direction.pollFirst();
		} 
		}
		

	}// end of method

	private static boolean wallChecking(int r, int c) {
		if (r < N && 0 <= r && c < N && 0 <= c) {
			return true;
		}
		return false;
	}

//클래스 선언 (Dir, Snake)
	public static class Dir {
		int time;
		char dir;

		public Dir(int time, char dir) {
			super();
			this.time = time;
			this.dir = dir;
		}
	}

	public static class Snake {
		int r;
		int c;
		int dir;

		// 만약, dir이 1이면 오른쪽, 2이면 위쪽, 3이면 왼쪽, 4이면 아래쪽
		public Snake(int r, int c, int dir) {
			super();
			this.r = r;
			this.c = c;
			this.dir = dir;
		}
	}// end of
}// end of class
```

뱀 문제는 뱀의 머리 위치와 꼬리 위치를 가변적으로 변경해야하는 문제이기 때문에 덱을 활용하면 좀 더 쉽게 구현할 수 있습니다.

**뱀의 머리 위치는 계속 덱에 위치들을 넣고,**  (deque.add(new Snake ~ 부분입니다.)

**사과가 없는 경우, pollLast() 함수를 사용하여 뱀의 꼬리 위치를 지우는 점이 핵심이라고 할 수 있습니다 😉**

**수정해야할 부분이 있거나 보완해야하는 사항이 있다면 언제든지 말씀해주세요!**

### 📕 Reference

[[자료구조\] 스택(Stack), 큐(Queue), 덱(Deque)](https://velog.io/@choiiis/자료구조-스택Stack과-큐Queue)

[[Java(자바)\] Deque(덱/데크) 자료구조](https://soft.plusblog.co.kr/24)

https://choijiuen.tistory.com/110

[[JAVA\] Queue 관련 함수 (+ 함수 차이점)](https://conanglog.tistory.com/217)

https://lemonlemon.tistory.com/40