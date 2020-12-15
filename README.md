# Git 연습하기

> 실 사용할 만한 git 명령어 연습하기

1. push 전의 commit message 수정하기

```
git commit --amend

# 입력창이 나오면서 최상단 commit message를 수정해주면됩니다.

# 저장하고 나온 이후
git push
```

2. push한 바로 전 commit message 수정하기

```
git commit --amend

# 입력창이 나오면서 최상단 commit message를 수정해주면됩니다.

# 저장하고 나온 이후에 내용이 수정되었기 때문에 강제 push를 진행해야합니다. ( 주의해야 할 점은 중간에 다른 사람의 push가 존재 하면 안됩니다. )
git push -f
```

3. 한참 전의 commit message 수정하기

```
git log --oneline

# hash와 현재 위치, commit message가 보입니다.  이때 고치고 싶은 commit message의 이전 hash를 복사합니다.

git rebase -i [hash]

# 다음과 같이하면 그 시점이후의 hash와 commit message가 보입니다.  수정하고 싶은 commit message 앞에 pick이라는 단어를 edit로 변경 후 저장합니다.

git commit --amend

# edit로 변경한 commit message가 보이고,  내용을 수정하고 저장합니다.

git rebase --continue

# reabse를 종료하고 내용이 변경되었기때문에
```
