# CS 지식을 학습하고 내용을 공유하기 위한 저장소입니다.

[스터디 소개](https://www.notion.so/thxwelchs/b6302126e9cb4119ada036adae44114e)

## 학습 자료 올리는 법
1. 해당 저장소를 clone 합니다.
    ```bash
    $ git clone https://github.com/cobak-study/computer-science.git
    ```
2. 해당 저장소 디렉토리로 이동 후 본인만의(본인이름) 브랜치로 체크아웃 합니다.
    ```bash
    $ git checkout -b {본인이름}(예시: taehun.lee)
    ```
3. MD(Markdown) 혹은 PDF, PPT와 같이 Github 상에서 Preview로 바로 볼 수 있는 형태의 확장자로 학습한 내용에 대해 글을 작성합니다.
4. 작성한 자료를 해당 주제에 맞는 디렉토리에 위치시킵니다.(디렉토리가 없다면 디렉토리를 생성해도 됩니다.)
\
`예:) Heap에 대해 학습했다면 DataStructure
5. 변경사항을 git stage 상에 올리고 commit 한다음 push 합니다.
    ```bash
    $ git add .
    $ git commit -m "[주제] 학습내용"
    $ git push origin {본인의 브랜치}
    ```
6. Github에서 Pull Request를 등록합니다.
- `New Pull Request` 초록 버튼을 클릭
![image](https://user-images.githubusercontent.com/38197077/113008009-a6496980-91b1-11eb-89eb-f898548ef64e.png)
- base 브랜치를 `master` compare 브랜치를 `{본인브랜치}`로 설정
![image](https://user-images.githubusercontent.com/38197077/113008201-caa54600-91b1-11eb-999f-89eaca475916.png)
- 제목과 내용에 대해 작성 후 `Create pull request`버튼을 클릭하여 PR 등록 __(의견을 나누고 싶거나 리뷰 받고싶은 대상이 있다면, Reviewers에 대상을 지정해주세요.)__
![image](https://user-images.githubusercontent.com/38197077/113008419-f9bbb780-91b1-11eb-889d-fa543a3b9e39.png)
7. 발표 후 질문받은 내용에 대해 해당 PR 페이지에 들어가 코멘트로 작성합니다. (질문자가 직접 해당 PR에 코멘트를 달거나, 질문자를 PR에 Reviewer로 걸어두면 더 좋습니다.)
![image](https://user-images.githubusercontent.com/38197077/113009033-8f574700-91b2-11eb-9860-5f2522e9340e.png)
8. 질문 받은 내용에 대해 학습자료에 수정한 내용이 있다면, 반영 후 다시 해당 브랜치로 PUSH(PUSH만 해도 PR에 알아서 반영이 됩니다.) 그리고 코멘트에 답변까지 달아주면 굿!
![image](https://user-images.githubusercontent.com/38197077/113009642-17d5e780-91b3-11eb-97d1-73713c03e192.png)
9. 학습내용에 대해 더이상 추가, 변경해야 할 사항이 없다면 master 브랜치로 Merge (해당 PR 페이지에서 `Merge pull Request` 버튼 클릭)
![image](https://user-images.githubusercontent.com/38197077/113009884-553a7500-91b3-11eb-8534-eaad7e9ad3ed.png)
