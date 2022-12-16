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
