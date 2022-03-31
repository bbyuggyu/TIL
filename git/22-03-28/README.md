STUDY


# Shell

- 운영체제의 커널과 사용자를 이어주는 소프트웨어
- bash(Bourne Again Shell): Brian Fox가 작성한 유닉스 쉘
    - 다양한 운영체제에서 기본 쉘로 채택
- zsh: Paul Falstad가 작성한 유닉스 쉘
    - sh 확장형 쉘
    - 현재까지 가장 완벽한 쉘


# Shell Commend

```shell
이동 $ cd Documents/
폴더 생성 $ mkdir dev
이동 $ cd ..
현재 디렉토리 $ pwd
파일 생성 $ touch readme.md
파일 이동 $ mv readme.md bin/
파일 복사 $ cp readme.md bin/
파일 바꾸기 $ mv readme.md ./README.txt
파일 삭제 $ rm README.txt
파일 하위까지 삭제 $ rm -rf bin/
파일 펼치기 $ cat readme.md
파일 편집기 $ vi readme.md
```

# Recap - Vim command

* i - insert mode
* v - visual mode
* ESC - back to normal mode
* d - delete

## Command mode

* :q - quit
* :q! - quit discarding all changes
* :w - write
* :wq - write and quit
* :{number} - jump to {number}th line.

