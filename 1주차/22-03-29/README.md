STUDY


# Creat TIL git file
```shell
$ mkdir git
$ cd git
$ mkdir 22-03-29
$ cd 22-03-29
$ mkdir 22-03-29.md
$ vi 220329---
```

# git process command

```shell
$ git add
$ git commit
$ git push origin main
```

Conventional commits
- 제목은 commit을 설명하는 하나의 구절로 작성
- 동작 가능한 최소 단위로 자주 할 것
- 모두가 이해 가능한 log를 작성 할 것
- 오프소스 경우 영어로, 그렇지 않은 경우 팀 내 사용 언어로 작성
- 제목과 내용은 한 칸 띄워서 작성
- prefix 꼭 달기
  - feat: 기능 개발 관련
  - fix: 오류 개선 or 버그 패치
  - docs: 문서화 작업
  - test: test 관련
  - conf: 환경설정 관련
  - build: 빌드 관련
  - ci: continuous integration 관련



# How to git push

method clone
- Creat repo
- git clone
- git add
- git commit
- git push
- git push origin main

method init
- git init
- git remote add origin https://github.com/{username}/{reponame}.git
- touch README.md
- git add README.md
- git commit
- git push -u origin main

