## Git 설치

> [git-scm.com](git-scm.com) 들어가서 **Download x.x.x for Window** 클릭  

## 버전관리의 시작

#### 버전관리 디렉토리

> 1. git bash 실행
> 2. 작업 디렉토리로 이동 (cd 명령어 사용)
> 3. git init 명령어 입력

#### git bash 콘솔에서 쓰는 다양한 명령어들

- git init : 이 디렉토리 이하에 대해 버전관리를 하겠다

- cat (파일명).txt

  - 실행시 빈 콘솔창(nano라는듯)으로 이동함
  - 거기서 txt파일 내용 작성/수정
  - 내용 다 입력 후 ctrl+x - Y - Enter 하면 작성/수정 완료

- **git status: 현상태 알랴줌(가장 많이 씀)**

- git add (파일명)

  - 수정된 버전을 기록할 파일 등록 (사진대에 올려놓는 것 비유)
  - 한 번만 add 해두면 이후에는 git commit -am "Commit 내용"으로 자동 Commit 가능
  - 한 번도 add 해두지 않았다면 git commit -am "Commit 내용"으로 자동 등록 불가

- git log

  - 버전들 나열해줌
  - git log --stat 하면 수정 내용도 알랴줌
  - git log - 이후 명령어(-stat등)로 다양한 리턴 받기 가능
    (변경일과 commit만 알려주는 것 부터, 파일 추가/제거 내역 등 까지)

- git diff

  - git log랑 비슷함
  - 가장 디테일하게(파일 내용) 알려주는듯

  





### GIT2 - CLI 버전관리 -7. checkout과 시간여행

> 코드, 파일, 문서를 수정하면서 의미있는 변경점을 기록하는 것

- 효용: 버전 기록

- git checkout (commit명) >> 해당 commit으로 시간여행
- git checkout master >>현재 commit으로 돌아옴
- ls -al (현재 디렉토리 내용 확인)

- git bash에서 파일 생성/내용 수정 
  1. nano (파일명)
  2. 내용 작성/수정
  3. ctrl+x - Y - Enter 

- git commit -am "4"  : add+ commit

  -add랑 commit을 동시에 해주는 명령어

  -1회라도 add 되지 않은 파일은 안됨



# git reset 

### git reset --hard versionCode

> 현재 수정중인 버전 지움. versionCode로 회귀 

### git reset --soft versionCode

> 현재 다루고 있는 버전은 남기고 이전 버전으로 돌아가고 싶다면 soft 쪽을 찾아보자

### git confit --global core.editor

> 편한 에디터를 사용하게 해줌



### git revert versionCode(git log 하면 나오는 것)

> 수행시 해당 versionCode 전의 버전으로 돌아갑니다.  
>
> 버전 1>2>3>4 순으로 있을 때, 버전 1로 돌아가고자 한다면,  
>
> ​	git revert 2를 바로 하는 것이 아닌
>
> ​	git vert4>3>2 순으로 역순으로 해야 충돌하지 않는다고 함  
>
> ​	(머라는지 잘 모르겠음)  

