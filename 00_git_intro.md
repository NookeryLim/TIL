### Git 초기 설정

커밋 작성자(author) 설정

```bash
$ git config --global user.email "메일주소"
$ git config --global user.name "유저네임"
```

- 커밋을 작성하는 사람이 누구인지 알아야하기 때문

<br>

지정된 설정 확인

```bash
$ git config --global -l
# 또는 $ git config --global -list

```

<br>

커밋 편집기 변경

```bash
$ git config --global core.editor "code --wait"
```

- 해당 명령어는 반드시 vscode가 설치되어 있어야 함

> 기본 텍스트 편집기 `vim`을 `vscode`로 대체하는 것

<br>

---

## Git Basic

### 로컬 저장소 설정

```bash
$git init
```

- 폴더에 git 저장소를 초기화하면
  - `.git`숨김 폴더가 생기고
  - bash에는 `(master)`라고 표기된다.

> 주의사항
>
> - git 저장소 내에 또다른 git 저장소를 만들면 안됨!!
> - `git init` 명령어를 입력할 때, `(master)`가 있으면 절대 입력하지 말것!

<br>

### add

> staging area / INDEX

```bash
$ git add 파일명
$ git add . # 현재 디렉토리(하위 디렉토리 포함)
$ git add a.txt # 특정 파일
$ git add my_folder/ # 특정 폴더
```

- `working directory` 상태의 파일을 `staging area` 상태로 변경
- 커밋을 위한 파일 및 폴더들을 추가하는 명령어

```bash
$ touch a.txt b.txt

$ git status
# 다른점 붙여넣기
```

```bash
$ git  add a.txt
```

```bash
$ git status
```

> 모든 정보는`git status`에 있다.

<br>

### commit

```bash
$ git commit -m "first commit"
```

- 커밋을 통해 하나의 버젼으로 기록됨
- 커밋 메세지는 현재 변경사항들을 잘 나타낼 수 있도록 작성하는 것을 권장
- 커밋은 고유한 아이디인 해시 값을 가짐
  - SHA-1 알고리즘에 의해 생성
- 커밋 목록은 `git log`를 통해서 확인할 수 있음

```bash
$ git log --oneline #커밋 목록 한 줄로 보기
```



---

### 추가 커밋 쌓기

- a.txt 내용 수정

```bash
$git status
```









