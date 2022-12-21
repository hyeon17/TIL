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

## Start Project with git clone
### github Conventional Commits
- `commit`의 제목은 `commit`을 설명하는 하나의 구나 절로 완성 feat: 기능 개발 관련

```Markdown
fix: 오류 개선 혹은 버그 패치
docs: 문서화 작업
test: test 관련
conf: 환경설정 관련
build: 빌드 관련
ci: Continuous Integration 관련
```

  - 예시)
 ```Markdown
 feat: Add server.py
fix: Fix Typo server.py
docs: Add README.md, LICENSE
conf: Create .env, .gitignore, dockerfile
BREAKING CHANGE: Drop Support /api/v1
refactor: Refactor user classes
```


### README.md
- 프로젝트와 Repository를 설명하는 책의 표지와 같은 문서
- 나와 동료, 이 repo의 사용자를 위한 문서

### .gitignore
- .gitignore 는 git이 파일을 추적할 때, 어떤 파일이나 폴더 등을 추적하지 않도록 명시하기
위해 작성, 해당 문서에 작성된 리스트는 수정사항이 발생해도 git이 무시
- 특정 파일 확장자를 무시하거나 이름에 패턴이 존재하는 경우, 또는 특정 디렉토리 아래의 모
든 파일을 무시.
- 사용 시 https://www.toptal.com/developers/gitignore 에서 사용하는것을 권장
  - 사용 예시)
  ![](https://velog.velcdn.com/images/hyeon_17/post/9af0b3ee-5146-4143-a9a0-8f254df32f54/image.png)
    > 사용 환경이 windows, macos, vsc, react일 경우 항목들을 추가 하고 생성 버튼 클릭
      
   ![](https://velog.velcdn.com/images/hyeon_17/post/2d56b0b8-e14e-41ba-a27a-749d04d53ef0/image.png)
    > 생성이 완료되면 위와 같은 항목들이 생성됨. 복사하여 .gitignore 파일에 붙여넣기


### LICENSE
- MIT License
  - MIT에서 만든 라이센스로, 모든 행동에 제약이 없으며, 저작권자는 소프트웨어와
관련한 책임에서 자유롭다.
- Apache License 2.0
  - Apache 재단이 만든 라이센스로, 특허권 관련 내용이 포함.
- GNU General Public License v3.0
  - 가장 많이 알려져있으며, 의무사항(해당 라이센스가 적용된 소스코드 사용시 GPL
을 따라야 함)이 존재

## Branch
- 분기점을 생성하여 독립적으로 코드를 변경할 수 있도록 도와주는 모델
- 브랜치 옵션
  > checkout: 브랜치 전환 또는 작업 트리 파일 복원
switch: 브랜치 전환
restore: 작업 트리 파일 복원
### Branch 사용법 및 설명
- 사용 가능한 로컬 브랜치 표시
  - `$ git branch`
- 사용 가능한 원격 브랜치 표시
  - `$ git branch -r`
- 사용 가능한 모든 브랜치 표시
  - `$ git branch -a`
- stem이라는 이름을 가진 브랜치 만들기
  - `$ git branch stem`
- stem브랜치 전환
  - `$ git switch stem`
- new-stem브랜치 생성과 체크아웃
  -`$ git checkout -b new-stem`
- readme.md 내부에서 변경
  - `$ git commit -a -m 'edit readme.md'`
  - `$ git checkout master`
- stem브랜치 병합
  - `$ git merge stem`
- 브랜치 삭제
  - `$ git branch -D stem`
- 지정된 원격 브랜치로 푸시
  - `$ git push origin stem`
- 두 브랜치의의 차이를 보기
  - `$ git diff master stem`
  
### branching models
- git flow
  - (hotfix)- master -(release)- develop - feature
  - pros: 가장 많이 적용, 각 단계가 명확히 구분
  - cons: 복잡..
- github flow
  - master - feature
  - pros: 브랜치 모델 단순화, master 의 모든 커밋은 deployable
  - cons: CI 의존성 높음. 누구 하나라도 실수했다간..(pull request로 방지)
- gitlab flow
  - production - pre-production - master - feature
  - pros: deploy, issue에 대한 대응이 가능하도록 보완
  - cons: git flow와 반대 ( master -develop, production -master)

### git flow strategy
![](https://velog.velcdn.com/images/hyeon_17/post/de0cfdb7-4afd-4f17-aeb6-402126d85a23/image.png)

### git flow 사용법
![](https://velog.velcdn.com/images/hyeon_17/post/bb86e5dd-6c76-4b52-a295-72c86f0a05d2/image.png)

#### Main Branches  
1.Master 
- 제품으로 출시될 수 있는 브랜치 (main) 
- master의 최신버전은 언제나 실행가능해야함 

2.Develope
- 실행가능한 상태를 만들어가는 과정
- 다음 출시 버전을 개발하는 브랜치

#### Temporary Branches
- merge 된 후 사라지는 임시 브랜치

3.feature 
- 기능 개발하는 브랜치 
- feature/기능명 으로 생성하고 사용 후 삭제 

4.Release 
- 이번 출시 버전을 준비하는 브랜치 
- release/버전명 으로 생성하고 사용 후 삭제 
- QA, TEST etc.. 

5.Hotfixes
- 출시한 버전에 긴급하게 수정해서 다시 업데이트 해야할 때 
- hotfixes/차기 버전명 으로 생성하고 사용 후 삭제 
- bugfix 

> git-flow 개발 프로세스  예시
1.개발자는 develop branch로부터 본인이 개발할 기능을 위한 feature branch 생성
2.feature branch에서 기능을 만들다가 기능 완성후에 develop branch에 merge
3.이번 배포 버전의 기능들이 develop branch에 모두 merge 되었다면 QA, TEST를 위해 release 브랜치 생성 
4.release branch에서 오류가 발생한다면 release 브랜치 내에서 수정 , QA 가 끝났다면 해당 버전을 배포하기 위해 master branch로 merge한다. bugfix가 있었다면 해당 내용을 반영하기 위해 develop branch에도 merge
5.만약 제품 (master)에서 버그가 발생한다면 hotfix branch 생성
6.hotfix branch에서 bugfix 끝나면 develop과 master branch에 각각 merge 

#### 개발 프로세스
- git flow 초기화를 진행하면 develop 브랜치가 생성되고 전환됨
  - `$ git flow init`
- feature/flow-test 브랜치가 생성
  - 기능 하나를 개발할때마다 feature브랜치를 열고 닫아야 함
  - `$ git flow feature start flow-test`
- feature/flow-test 브랜치가 종료
  - 종료된 즉시 feature/flow-test브랜치는 자동 삭제됨
  - `$ git flow feature finish flow-test`
- team 저장소에서 코드를 가져올때
  - `$ git remote add <저장소 이름> <저장소 주소>`
  
git pull = git fetch + git merge
pull과 fetch의 차이점은 병합을 하냐 안 하냐의 차이

1. git pull
원격저장소에 있는 프로젝트의 변경사항을 그대로 로컬저장소에 옮겨와 자동으로 병합
변경 사항을 가져옴과 동시에 자동으로 병합이 되기 때문에 무엇이 추가되고 병합되었는지 확인이 안 됨

2. git fetch
다른 사람이 수정한 부분을 확인하고 병합할 수 있다는 장점




## Revert
### Rename
