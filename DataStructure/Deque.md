# Deque (๋ฑ/๋ฐํฌ)

## **๐ ๋ชฉ์ฐจ**

------

### โDeque ์ ์

### ๐๐ปโโ๏ธ Deque ๋ด์ฅ ํจ์

### **โจ ๋ฌธ์ ์ ์ ์ฉํด๋ณด๊ธฐ**

------

์ฐ์ ,  ์ด ๋ธ๋ก๊ทธ๋ค์ ๋ณด๋ฉด์ **๊ณต๋ถํ๋ ๋ด์ฉ์ ์ ๋ฆฌํ ๊ธ**์ด๋ผ๋ ์ ์ ๋ง์๋๋ฆฝ๋๋ค! ๐

[[์๋ฃ๊ตฌ์กฐ\] ์คํ(Stack), ํ(Queue), ๋ฑ(Deque)](https://velog.io/@choiiis/์๋ฃ๊ตฌ์กฐ-์คํStack๊ณผ-ํQueue)

[[Java(์๋ฐ)\] Deque(๋ฑ/๋ฐํฌ) ์๋ฃ๊ตฌ์กฐ](https://soft.plusblog.co.kr/24)

[Queue offer๊ณผ add์ ์ฐจ์ด](https://choijiuen.tistory.com/110)

[[JAVA\] Queue ๊ด๋ จ ํจ์ (+ ํจ์ ์ฐจ์ด์ )](https://conanglog.tistory.com/217)

https://lemonlemon.tistory.com/40

### โDeque ์ ์

![Deque](https://images.velog.io/images/esun1903/post/3f91d93c-ce79-4d20-9ce8-d7395b282af4/image.png)

- `Deque(Double Ended Queue)`, `queue`์ ๋น์ทํ์ง๋ง `queue`๋ `front`์์๋ง ์ญ์ ํ๊ณ , `end`์์ ์ฝ์ํ๋๋ฐ, `deque`๋ `front`์ `end`์์ ์ญ์ ์ ์ฝ์์ด ๋ชจ๋ ๊ฐ๋ฅํ๋ค.
- ์ฐ์์ ์ธ ๋ฉ๋ชจ๋ฆฌ๋ฅผ ๊ธฐ๋ฐ์ผ๋ก ํ๋ '์ํ์ค ์ปจํ์ด๋'์ด๋ค. ๋ฐ๋ผ์, ์์ ์ ๊ทผ ๋ฐ๋ณต์ ์ ๊ณต.
- ์ฌ๋ฌ ๊ฐ์ ๋ฉ๋ชจ๋ฆฌ ๋จ์๋ก ๋ฐ์ดํฐ๋ฅผ ์ ์ฅํ๋ค. vector๋ ๋ฉ๋ชจ๋ฆฌ๋ฅผ ์ฌํ ๋นํ๊ณ  ๋ชจ๋  ์์๋ฅผ ๋ณต์ฌํ์ฌ์ผ ํ๋๋ฐ, deque๋ ์๋ก์ด ๋ฉ๋ชจ๋ฆฌ ๋จ์๋ฅผ ํ ๋นํ์ฌ ์์๋ฅผ ์ถ๊ฐํ๋ค.๋ ๋ฐ์ดํฐ ์์๋ฅผ ์ ์ฅํ๋ ์ฌ๋ฌ ๊ฐ์ ๋ฉ๋ชจ๋ฆฌ ๋จ์๋ฅผ ๊ฐ์ต๋๋ค.
- ํฌ๊ธฐ๊ฐ ๊ฐ๋ณ์ ์ด๋ค. (์ ์ธ ํ์ ๋ณ๊ฒฝํ  ์ ์๋ค.)
- ์ค๊ฐ ์์๊ฐ ์ฝ์, ์ญ์ ๋  ๋, ์์๋ค์ ์/๋ค๋ก ๋ฐ ์ ์์ผ๋ฏ๋ก vector๋ณด๋ค๋ ์ข์ ์ฑ๋ฅ์ ๊ฐ์. ๊ทธ๋๋, ์/๋ค์์์ ์ฝ์/์ญ์  ์ฑ๋ฅ์ ์ข์ง๋ง ์ค๊ฐ์์๋ ์ข์ง ์๋ค.

### ์๊ฐ ๋ณต์ก๋

์ฝ์/์ญ์ - ์์๋ฅผ ์/๋ค์ ์ฝ์ํ๋ ๊ฒฝ์ฐ : O(1)

์์๋ฅผ ์/๋ค์ ์ฝ์ํ๋ ๊ฒฝ์ฐ : O(1)

ํ์- ์์๋ฅผ ํ์ํ๋ ๊ฒฝ์ฐ : O(1) (index ์ ๊ทผ)

### ์ฅ์ 

๋ฐ์ดํฐ์ ์ฝ์๊ณผ ์ญ์ ๊ฐ ๋น ๋ฅด๋ค.

ํฌ๊ธฐ๊ฐ ๊ฐ๋ณ์ ์ด๋ค.

์, ๋ค์์ ๋ฐ์ดํฐ๋ฅผ ์ฝ์/์ญ์ ํ  ์ ์๋ค.

index๋ก ์์ ์์ ์ ๊ทผ์ด ๊ฐ๋ฅํ๋ค.

์๋ก์ด ์์ ์ฝ์ ์์, ๋ฉ๋ชจ๋ฆฌ๋ฅผ ์ฌํ ๋นํ๊ณ  ๋ณต์ฌํ์ง ์๊ณ  ์๋ก์ด ๋จ์์ ๋ฉ๋ชจ๋ฆฌ ๋ธ๋ก์ ํ ๋นํ์ฌ ์ฝ์ํ๋ค.

### ๋จ์ 

deque์ ์ค๊ฐ์์์ ์ฝ์๊ณผ ์ญ์ ๊ฐ ์ด๋ ต๋ค.๊ตฌํ์ด ์ด๋ ต๋ค.

### ๐๐ปโโ๏ธ Deque ๋ด์ฅ ํจ์

**๋ฑ์ ์ ๋ถ๋ถ์ ๊ฐ์ ์ถ๊ฐํ๊ธฐ**

- addFirst()
- offerFirst()

**๋ฑ์ ๋ท ๋ถ๋ถ์ ๊ฐ์ ์ถ๊ฐํ๊ธฐ**

- addLast()
- add()
- offerLast()
- offer()

์ฌ๊ธฐ์, add์ offer์ ์ฐจ์ด๋ ๋ฌด์์ผ๊น์?

- add ๋ฉ์๋:  illegalStateException๋ฅผ ๋ฐ์์ํจ๋ค.
- offer ๋ฉ์๋ : ํ๊ฐ ๊ฐ๋์ฐจ์ ๋์ด์ ์ถ๊ฐํ  ์ ์๋ ๊ฒฝ์ฐ false๋ฅผ ๋ฐํํ๊ณ  ์์๊ฐ ์ถ๊ฐ๋๋ฉด true๋ฅผ ๋ฐํํ๋ฉฐ ํน์  ์์ธ๋ฅผ throwํ์ง ์๋๋ค.

**๋ฑ์ ์ ๋ถ๋ถ์ ๊ฐ์ ์ญ์ ํ๊ธฐ**

- remove()
- removeFirst()
- pollFirst()
- poll()

**๋ฑ์ ๋ท ๋ถ๋ถ์ ๊ฐ์ ์ญ์ ํ๊ธฐ**

- removeLast()
- pollLast()

์ฌ๊ธฐ์, remove์ poll์ ์ฐจ์ด๋ ๋ฌด์์ผ๊น์?

- remove ๋ฉ์๋ :  ํ๊ฐ ๋น์ด์์ ๋ ์ญ์ ํ๋ฉด ์์ธ ๋ฐ์ํฉ๋๋ค.
- poll ๋ฉ์๋ : ํ๊ฐ ๋น์ด์์ ๋ ์ญ์ ํ๋ฉด null์ ๋ฐํํฉ๋๋ค.

**๋ฑ์ ์ ๋ถ๋ถ์ ๊ฐ์ ๊ฐ์ ธ์ค๊ธฐ (์ฝ๊ธฐ)**

- getFirst()
- peekFirst()
- peek()

**๋ฑ์ ๋ท ๋ถ๋ถ์ ๊ฐ์ ๊ฐ์ ธ์ค๊ธฐ (์ฝ๊ธฐ)**

- getLast()
- peekLast()

์ฌ๊ธฐ์, get๊ณผ peek์ ์ฐจ์ด๋ ๋ฌด์์ผ๊น์?

- get ๋ฉ์๋ :  ํด๋น ๊ฐ์ return ํ๊ณ  ์คํจ ์ Exception์ ๋ฐ์์ํต๋๋ค.
- peek ๋ฉ์๋ : ๊ธฐ๋ณธ ์ ์ผ๋ก ํด๋น ๊ฐ์ ๋ฐํํ๋ค๋ ์ ์์ get๊ณผ ๋น์ทํ์ง๋ง, ์คํจ ์์ null์ returnํ๋ค๋ ์ ์ด ์ฐจ์ด์ ์๋๋ค.

### **โจ ๋ฌธ์ ์ ์ ์ฉํด๋ณด๊ธฐ**

๊ทธ๋ผ, ์ฌ๊ธฐ์ deque๋ฅผ ์ฌ์ฉํ์ฌ ํ ์ ์๋ ๋ฌธ์ ๋ค์ ๋ณด๋ฉฐ ์ ์ฉํด๋ณด์์! ๐

[3190๋ฒ: ๋ฑ](https://www.acmicpc.net/problem/3190)

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
			board[r-1][c-1] = 2; // ์ฌ๊ณผ์ ์์น
		}

		L = Integer.parseInt(br.readLine());
		// ๋ฑ์ ๋ฐฉํฅ ๋ณํ ์ ๋ณด
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

		// ๋จธ๋ฆฌ ๋ฐฉํฅ๋๋ก ๊ธฐ์ด๊ฐ์ผํจ
		while (true) {
			Snake snake = deque.getFirst();
 
			int r = snake.r;
			int c = snake.c;
			int dir = snake.dir;
			// 1,1๊บผ๋์ด
			if (dir == 1) { // ๋ฐฉํฅ์ด ์ค๋ฅธ์ชฝ์ผ๋,
				c += 1;
			} else if (dir == 2) { // 2์ด๋ฉด ์์ชฝ
				r -= 1;
			} else if (dir == 3) { // 3์ด๋ฉด ์ผ์ชฝ
				c -= 1;
			} else if (dir == 4) { // 4์ด๋ฉด ์๋์ชฝ
				r += 1;
			}
			time++;
			if (wallChecking(r, c) == true && board[r][c] != 1) {
				// ์ฌ๊ณผ๊ฐ ์์ ๋,
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

//ํด๋์ค ์ ์ธ (Dir, Snake)
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

		// ๋ง์ฝ, dir์ด 1์ด๋ฉด ์ค๋ฅธ์ชฝ, 2์ด๋ฉด ์์ชฝ, 3์ด๋ฉด ์ผ์ชฝ, 4์ด๋ฉด ์๋์ชฝ
		public Snake(int r, int c, int dir) {
			super();
			this.r = r;
			this.c = c;
			this.dir = dir;
		}
	}// end of
}// end of class
```

๋ฑ ๋ฌธ์ ๋ ๋ฑ์ ๋จธ๋ฆฌ ์์น์ ๊ผฌ๋ฆฌ ์์น๋ฅผ ๊ฐ๋ณ์ ์ผ๋ก ๋ณ๊ฒฝํด์ผํ๋ ๋ฌธ์ ์ด๊ธฐ ๋๋ฌธ์ ๋ฑ์ ํ์ฉํ๋ฉด ์ข ๋ ์ฝ๊ฒ ๊ตฌํํ  ์ ์์ต๋๋ค.

**๋ฑ์ ๋จธ๋ฆฌ ์์น๋ ๊ณ์ ๋ฑ์ ์์น๋ค์ ๋ฃ๊ณ ,**  (deque.add(new Snake ~ ๋ถ๋ถ์๋๋ค.)

**์ฌ๊ณผ๊ฐ ์๋ ๊ฒฝ์ฐ, pollLast() ํจ์๋ฅผ ์ฌ์ฉํ์ฌ ๋ฑ์ ๊ผฌ๋ฆฌ ์์น๋ฅผ ์ง์ฐ๋ ์ ์ด ํต์ฌ์ด๋ผ๊ณ  ํ  ์ ์์ต๋๋ค ๐**

**์์ ํด์ผํ  ๋ถ๋ถ์ด ์๊ฑฐ๋ ๋ณด์ํด์ผํ๋ ์ฌํญ์ด ์๋ค๋ฉด ์ธ์ ๋ ์ง ๋ง์ํด์ฃผ์ธ์!**

### ๐ Reference

[[์๋ฃ๊ตฌ์กฐ\] ์คํ(Stack), ํ(Queue), ๋ฑ(Deque)](https://velog.io/@choiiis/์๋ฃ๊ตฌ์กฐ-์คํStack๊ณผ-ํQueue)

[[Java(์๋ฐ)\] Deque(๋ฑ/๋ฐํฌ) ์๋ฃ๊ตฌ์กฐ](https://soft.plusblog.co.kr/24)

https://choijiuen.tistory.com/110

[[JAVA\] Queue ๊ด๋ จ ํจ์ (+ ํจ์ ์ฐจ์ด์ )](https://conanglog.tistory.com/217)

https://lemonlemon.tistory.com/40