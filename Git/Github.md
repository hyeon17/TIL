# Github

## git Process Flow and Command
![git Process](/img/git%20process.png)

## Local
### working directory
- untracked: 아직 tracking이 되지 않은 파일
  > 기존에 존재하던 프로젝트에서 git을 초기화하거나 파일을 새로 만들면(또는 처음 저장소를 clone하면) untracked 상태이다.

- tracked: unmodified/modified로 나눌 수 있다. checkout된 이후 수정사항이 있지만 stage되지 않으면 modified된 상태이다.
  > modified된 파일만 staging area로 옮겨갈 수 있다.

  ![working directory](/img/working%20directory.png)
- git add
  - 다음 변경(commit)을 기록할 때까지 변경분을 모아놓기 위해서 사용
  
### staging area
- tracked & staged 상태
- add 명령어를 통해 파일을 Staging Area에 올릴 수 있다.
- git rm --cached를 이용하면 unstage(Staging Area-> Working Directory)가 가능하다.
- git diff --cached는 index와 HEAD 사이의 변화를 보여준다.
- git commit
  - 깃이 코드 변화를 기록하는 것
- git switch
  - 브랜치를 변경(switch)하는 명령어
### local repo
- git 저장소(내 컴퓨터), remote repo로 가기 전 상태
- git push
- git pull
  
## Remote
### remote repo

## github 문서 작성법
docs:
