STUDY


# Rename

```shell
- Wost
    $ mv {file name} {file name}

- Best
    $ git mv {file name} {file name}
```
파일의 history를 남기기 위해서는 삭제 후 생성이 아닌 이름바꾸기로 추적

# Undoing

```shell
파일 내용 되돌리기: $ git restore
파일 모두 되돌리기: $ git restore .
add한 파일 내리기: $ git reset HEAD {파일이름}
add한 파일 내리기: $ git restore --staged {파일이름}
커밋 메세지 수정: $ git commit --amend
```

# Reset Commit

reset, revert, checkout

```shell
- Worst case: Reset
    ex) 직전 3개의 commit을 삭제한 후, remote에 강제 push
    $ git reset --hard HEAD~3
    $ git push -f origin <branch>
        - 협업 시 다른 cloned repo에 존재하던 commit log로 인해 파일이 살아나거나, 과거 이력이 깔끔히 사라져 commit log tracking이 힘들어짐.
        - solution: 잘못한 이력도 commit으로 박제하고 수정한 이력을 남기자!

- Best case: Revert
    ex) 현재 HEAD에서 직전의 3개의 commit을 순서대로 거슬러 올라가 해당 내역에 대해 commit, push 수행
    $ git revert --no-commit HEAD~3..
    $ git commit
    $ git push origin <branch>
        - 잘못하기 전 과거로 돌아가 최신을 유지하면서 되돌렸다는 이력을 commit으로 남겨 모든 팀원이 이 사항을 공유하고 주지시킬 수 있음.
        - commit을 따로 안할땐 --no-edit
        - merge commit을 되돌릴 땐 -m ( $git revert -m {1 or 2} {merge commit id} )

checkout
$ git checkout {commit id}
```

# reset, revert, checkout의 차이점

reset: 파일 내용과 commit 기록을 모두 삭제 후 되돌리기 (HEAD와 Branch 모두 이동)  
revert: 패일 내용은 삭제되지만 commit 기록은 남겨둔 채로 되돌리기  (HEAD와 Branch 모두 이동)  
checkout: 파일 내용 commit 기록 모두 유지하며 특정 커밋으로 이동. (HEAD만 이동)  

참고 링크
[git reset과 git checkout의 차이점] (https://blog.naver.com/codeitofficial/222011693376)

