# git Process Flow and Command
![](https://velog.velcdn.com/images/hyeon_17/post/4a13d1e2-acfa-4a0d-8919-b9243a3352a9/image.png)

## Local
### working directory
- untracked: 아직 tracking이 되지 않은 파일
  - 기존에 존재하던 프로젝트에서 git을 초기화하거나 파일을 새로 만들면(또는 처음 저장소를 clone하면) <span style="color: red">untracked</span> 상태이다.
<img src=https://velog.velcdn.com/images/hyeon_17/post/1ae105f9-efd4-4e3e-9618-615e1b7a6125/image.png>
빨간색 파일들이 Untracked 상태의 파일들

- tracked: unmodified/modified로 나눌 수 있다. `git status`명령어를 실행했을 때 Changes to be committed으로 바뀐것을 볼수있다.
  - modified된 파일만 staging area로 옮겨갈 수 있다.
	![](https://velog.velcdn.com/images/hyeon_17/post/7d061718-e81a-4477-9297-d1d1cd503f37/image.png)
초록색 파일들이 Staged 상태의 파일들
> tracked.txt 파일을 만들어 `git add`를 한 후 `git status`명령어를 실행한 화면

 ![](https://velog.velcdn.com/images/hyeon_17/post/f5ba3cfa-eeb1-4214-9c50-41b8936cf376/image.png)
#### git add
  - 다음 변경(commit)을 기록할 때까지 변경분을 모아놓기 위해서 사용
  - 사용법
    - 작업 디렉토리의 변경 내용의 일부만 스테이징 영역에 넘기고 싶을 때는 수정한 파일이나 디렉토리의 경로를 인자로 넘긴다
      > $ git add <파일/디렉토리 경로>
    - 현재 디렉토리의 모든 변경 내용을 스테이징 영역으로 넘기고 싶을 때는, `.`을 인자로 넘긴다
      > $ git add .
    - 작업 디렉토리 내의 모든 변경 내용을 전부 다 스테이징 영역으로 넘기고 싶을 때는, `-A` 옵션을 사용
      > $ git add -A
    - `-p`옵션은 각 변경 사항을 터미널에서 직접 눈으로 하나씩 확인하면서 스테이징 영역으로 넘기거나 또는 제외할 수가 있다. 많은 변경 내용을 여러 개의 변경 기록으로 나누어서 남기고 싶을 때 유용하게 사용
      > $ git add -p
      
     ##### 참고
    > `$ git add -A`는 작업 디렉토리 상에 어디에 위치하든 항상 동일하게 모든 변경 내용을 스테이징으로 넘깁니다. 반면에 `$ git add .`는 명령어를 실행한 디렉토리 이하에서 발생한 변경 내용만 포함하며, 해당 디렉토리 기준으로 상위 디렉토리의 변경 내용을 포함하지 않는다. 만약에 `$ git add .`를 프로젝트 최상위 디렉토리에서 실행한다면 `$ git add -A`와 동일하다.

  
### staging area
- tracked & staged 상태
- `add` 명령어를 통해 파일을 Staging Area에 올릴 수 있다.
- `$ git rm --cached`를 이용하면 unstage(Staging Area-> Working Directory)가 가능하다.
- `$ git diff --cached`는 index와 HEAD 사이의 변화를 보여준다.
#### git commit
  - 깃이 코드 변화를 기록하는 것
  - 동작하는 최소단위로 진행해야 한다
#### git switch
  - 브랜치(branch)를 변경(switch)하는 명령어
#### git status
- 작업 디렉토리(working directory)와 스테이징 영역(staging area)의 상태를 확인하기 위해서 사용

### local repo
- 내 PC에 파일이 저장되는 개인 전용 저장소
- remote repo로 가기 전 상태
#### git push
- 원격 저장소(remote repository)에 코드 변경분을 업로드하기 위해서 사용

#### git pull
- 원격 저장소에서 변경된 메타데이터 정보를 확인할 뿐만 아니라 최신 데이터를 복사하여 로컬 Git에 가져온다.

  
## Remote
### remote repo
- 파일이 원격 저장소 전용 서버에서 관리되며 여러 사람이 함께 공유하기 위한 저장소

## github Conventional Commits
- commit의 제목은 commit을 설명하는 하나의 구나 절로 완성
> feat: 기능 개발 관련
fix: 오류 개선 혹은 버그 패치
docs: 문서화 작업
test: test 관련
conf: 환경설정 관련
build: 빌드 관련
ci: Continuous Integration 관련

  - 예시)
>feat: Add server.py
fix: Fix Typo server.py
docs: Add README.md, LICENSE
conf: Create .env, .gitignore, dockerfile
BREAKING CHANGE: Drop Support /api/v1
refactor: Refactor user classes

git flow