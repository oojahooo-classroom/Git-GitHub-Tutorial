# Git-GitHub-Tutorial
Git &amp; GitHub Tutorial for Individual Project

## Clone Me!
Clone은 GitHub의 repo를 가져와 작업할 준비를 할 수 있도록 하는 가장 간편한 커맨드입니다.

원하는 디렉토리에서 다음을 실행하여 이 repo를 자신의 working directory에 local repo로 복제해 보세요:
```
git clone [link of this repository]
```

## Diff, Status
이제 복제한 repo를 직접 수정해볼 차례입니다!

이 `README.md` 파일의 아래 블럭 부분에 텍스트를 추가해 보세요:

```
아래 부분에 마음껏 글을 적어 보세요



위 부분에 마음껏 글을 적어 보세요
```

지금 수정한 부분이 local repo의 현재 commit과 얼만큼 다른지 궁금하다면, 다음 커맨드를 입력해 보세요:
```
git diff
```
만약 특정 파일이나 폴더에 대해서만 확인하고 싶다면, 위 커맨드의 뒤에 원하는 파일 또는 폴더 이름을 추가로 넣고 실행하면 됩니다.

만약 구체적인 내용이 아닌, 어떤 파일이 수정되었고 추가되었으며 삭제되었는지 확인하고 싶다면 다음의 커맨드를 입력해 보세요:
```
git status
```
이 때 git은 local repo의 현재 commit을 기준으로 현재 working directory에서 어떤 파일이 추가되었고, 수정되었고, 삭제되었는지 목록을 보여줄 것입니다.
지금은 `README.md` 파일만 수정했기 때문에 다음과 같은 결과가 출력될 것입니다:
```
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```

## Add - Commit - Push
미련 없이 글을 전부 썼다면, 이제 이 수정사항을 commit으로 남겨 저장해 봅시다.

자신의 작업 공간(working directory)에서 새로 수정한 부분을 local repo에 반영하기 위해선, 일단 장바구니의 역할을 하는 staging area에 수정한 파일(또는 일부분)을 추가해야 합니다.
다음을 실행해 `README.md` 파일을 stage시켜 봅시다:
```
git add README.md
```
만약 `README.md` 파일 뿐만 아니라 여러 파일을 수정했고, 모든 수정사항을 한 번에 stage시키고 싶다면 위 커맨드에서 파일 이름 대신 `-A` 옵션을 넣어 실행하면 됩니다.

이제 `README.md`는 지금까지의 수정사항 그대로 staging area에 담겨있을 겁니다.
이 때 `git status`를 실행해 보면, `Changes to be committed:` 목록에 `README.md` 파일이 생겼을 것입니다.

다음은 stage시킨 수정사항을 local repo에 실제로 commit할 차례입니다.
다음을 실행해 stage된 수정사항을 commit해 보세요:
```
git clommit -m "[commit message]"
```
