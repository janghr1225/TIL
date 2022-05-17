# 오늘의 TIL



## 1. CLI 기초

- **git 설치**
  - git과 github
- **GUI와 CLI의 차이**
  - GUI (Graphic User Interface) : 그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식
  - CLI (Command Line Interface) : 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식
- **루트, 홈 디렉토리**
  - /  루트 디렉토리, 보통 c 드라이브
  - ~ 홈 디렉토리(틸드)
- **절대경로, 상대경로**
- **터미널 명령어**
  - touch
  - mkdir
  - ls
  - mv
  - cd
  - rm



## 2. Markdown

**마크다운이란?**

> 일반 텍스트 기반의 경량 마크업 언어

> 마크업을 더 쉽고 간단하게 사용하고자 만들어짐

> .md 확장자



- **마크다운 문법**
  1. 제목 : # 사용
  2. 목록 
     - 순서가 없는 목록 : - , * , + 사용
     - 순서가 있는 목록 : 1. 2. 3. 같은 숫자로 표기
     - tab키로 들여쓰기 가능
  3. 강조
  4. 코드
  5. 링크
  6. 이미지
  7. 인용
  8. 표
  9. 수평선



## 3. Git

- **Git 초기 설정** - 최초 한번만 설정

1. 누가 커밋 기록을 남겼는지 확인할 수 있도록 이름, 이메일 설정

```bash
$ git config --global user.name "이름"
$ git config --global user.email "메일 주소"
```

2. 올바르게 설정되었는지 확인

```bash
$ git config --global -l

또는

$ git config --global --list
```



- **기본 명령어**
  - git init
  - git status
  - git add
  - git commit
  - git log

![](https://hphk.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fc86c667a-616f-45b6-892e-15da6a3c494e%2FUntitled.png?table=block&id=e455d5aa-a031-431f-a091-210b3d9d2842&spaceId=daa2d103-3ecd-4519-8c30-4f55e74c7ef4&width=2000&userId=&cache=v2)



## 4. Github

- **원격 저장소(Remote Repository) 만들기**

  1. Github에서 원격 저장소 생성

  2. 로컬 저장소와 원격 저장소 연결

     1. 원격 저장소가 잘 생성되었는지 확인 후, 저장소의 주소를 복사합니다.

     2. 기존에 실습 때 만들었던 홈 디렉토리의 TIL 폴더로 가서 vscode를 엽니다.

     3. git init을 통해 TIL 폴더를 로컬 저장소로 만들어줍니다.

        ```bash
        $ git init
        Initialized empty Git repository in C:/Users/kyle/TIL/.git/
        ```

     4. git remote

        1. 등록
        2. 조회
        3. 삭제

  3. 원격 저장소에 업로드

     1. 로컬 저장소에서 커밋 생성

        ```bash
        $ git add day1.md
        $ git commit -m "Upload TIL Day1"
        [master (root-commit) f3d6d42] Upload TIL Day1
         1 file changed, 0 insertions(+), 0 deletions(-)
         create mode 100644 day1.md
         
         # 커밋 확인
        $ git log --oneline
        f3d6d42 (HEAD -> master) Upload TIL Day1
        ```

     2. git push

        ```bash
        $ git push origin master
        
        $ git push -u origin master
        이후에는 $ git push 라고만 작성해도 push가 됩니다.
        ```