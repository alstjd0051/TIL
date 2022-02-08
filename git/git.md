# [Git](https://git-scm.com/)

# 1. 설치

- [Git](https://git-scm.com/) 홈페이지로 들어가 download 한다.
- home brew를 이용하여 다운로드

```bash
$ brew install git
```

- [Binary installer](https://sourceforge.net/projects/git-osx-installer/files/git-2.33.0-intel-universal-mavericks.dmg/download?use_mirror=autoselect) 이용하여 설치

# 2. git 이용하기

```bash

git init
git config --global core.autocrlf input //맥을 이용하는 사람
git config --global core.autocrlf true //윈도우를 이용하는 사람
git config --global user.name '유저이름 설정'
git config --global user.email '유저이메일 설정'
git config --global --list // 이름과 이메일 설정확인
git status // 현재 프로젝트의 버전관리 상태확인
git add . // 등록하기
git commit -m "메시지 입력"
git log // 커밋내용 확인하기

```

# 3. git 저장소에 올리기

```bash
git remote add origin "레파지토리 url"
git push origin master // git에 올리기

```

# git hub 사용하기

- git hub를 자유롭게 사용하기 위한 여러 tool이 있다. ([git bash](https://git-scm.com/downloads) , [sourcetree](https://www.sourcetreeapp.com/) , [githubdesktop](https://desktop.github.com/), [kraken](https://www.gitkraken.com/))
- 하지만 나는 gitbash를 이용해 터미널로 쉽게 정리를 하겠다.

### git 시작

> ```bash
> # 개행문자 (Newline)설정
> ## macOS
> $git config --global core.autocrlf input
>
> ## Windows
> $git config --global core.autocrlf true
>
> #사용자 정보
> ## 커밋(버전 생성)을 위한 정보 등록
> $git config --global user.name "이름"
> $git config --global user.email "이메일"
>
> #구성 확인
> ## Q키를 눌러서 종료
> $git config --global --list
> ```

### 버전관리

> ```bash
> $git init # 현재 프로젝트에서 변경사항 추적(버전관리)을 시작
> $git add . #모든 파일의 변경사항을 추적하도록 지정.
> # or
> $git add 파일명.확장자 # 변경사항을 추적할 특정파일(파일명.확장자)을 지정
> $git commit -m "프로젝트 메시지" # 메시지(-m)와 함께 버전을 생성
> $git remote add origin "해당 레파지토리 url" # origin이란 별칭으로 원격 저장소를 연결
> $git status # git 파일상태 확인하기
> $git push origin "브렌치명" #origin이란 별칭의 원격저장소로 버전 내역 전송
> ```

### 브랜치관리

> ```bash
> $git branch #branch목록 확인
> $git branch -a # 브랜치목록확인
> $git branch "브랜치명" # 브랜치생성
> $git checkout "브랜치명" # 브랜치 이동
> ```

### 버전 되돌리기(Reset)

> ```bash
> $git reset --hard HEAD~1 # 이전 커밋한 내용을 되돌리겠다.
> ```
