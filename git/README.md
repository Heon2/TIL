# Unix/Linux 명령어
- **파일과 문서 보기** : ls

- **파일로 이동** : cd (파일명)

- **상위문서로 이동** : cd ..

- **파일생성** : mkdir (파일명)

- **파일삭제** : rm - r (파일명)

- **문서생성** : touch (문서명)

- **문서삭제** : rm (문서명)



# git 명령어

- **git init** : 깃에게 이 파일을 버전관리 시작하라는 명령어 (해당 파일 경로에 들어가서 명령어 입력)

- **git log** : 지금까지 만들어진 commit들을 볼 수 있다.

- **git status **: 현재 수정된 파일이 있는지 알려준다.

- **git diff (____) (____)** : 커밋코드 4자리를 확인후 입력하면 이전 버전과 달리진 점을 보여준다(사라진 것은 빨간색, 추가된 것은 초록색)

- **git add (파일명)** : (파일명)이 commit 하기전에 staging area에 올라간다.

- **git add .** : 모든 파일이 commit 하기전에 staging area에 올라간다.

- **git restore --staged (파일명)** : add했던 파일을 내림

- **git commit -m "수정하고 싶은 이름"** : commit을 하고 commit 이름이 "수정하고 싶은 파일"로 저장된다.

- **git restore (파일명)** : 최신버전의 commit으로 돌아간다.(수정한 작업이 취소됨)

- **git reset --hard (commit 코드 4자리)** : 해당 commit으로 돌아간다.

- **git config --global user.email** : 깃허브의 이메일 주소를 입력한다.

- **git config --global user.name** : 깃허브의 user name을 입력한다.

- **git remote add origin (remote_repo_url)** : remote repo를 local로 복사합니다.

- **git remote rm origin** : remote repo 연결을 해제

- **git push -u origin master** : 처음 연결을 할때 계정에 로그인하기위한 명령어

- **git push origin master** : local repo의 최신 커밋을 remote repo로 push합니다.

- **git push** : 연결이 되있는 상태면 push만 쳐도 됨

- **git pull origin master** : remote repo의 최신 버전을 가져옵니다.

- **git clone (remote_repo_url)** : remote repo를 내 local에 복사합니다.

- **git clone (remote_repo_url) .** : remote repo를 내 local에 복사합니다.(새로운 폴더 생성 x)

  [git 작성법 자료](http://aidenlim-edu.github.io/class-git-basic)



# github에 연결하기

github에 repository를 생성한다.

1. git bash로 연결 : 폴더생성 -> git init -> 파일생성 -> git add . -> git commit -m "파일명" -> git remote add origin (repo_url) -> git push origin master
2. 클론으로 연결 : git clone (repo_url)



##### git 공유 작업하는법(Shared Repository Model)

1. master일 경우 : 

   github에 repo생성 -> 폴더 생성 -> git init -> 파일 생성 -> git add . -> git commit -m "파일명" -> git remote add origin (repo_url) -> git push origin master -> github repo에서 setting -> mansge access -> invite a collaborator 클릭 

   

2. collaborator일 경우 :

   초대받으면 이메일에서 수락 -> git clone(repo_url)

# .gitignore

특정 파일들을 커밋하지 않는 방법

git파일이 있는곳에 touch .gitignore 생성

**.gitignore 안에 특정 문구를 넣어주면 제외 가능**

> data.csv  # 특정 파일 
>
> secret/    # 특정 폴더
>
> *.png       # 특정 확장자
>
> !profile.png  # 모든 profile.png빼고 나머지 png 제외



gitignore.io  ->  gitignore 만드는 것을 도와주는 사이트



# Branch

- **git branch (branch name)** : branch 생성
- **git checkout (branch name)** : branch 이동
- **git branch checkout -b (branch name)** : branch 생성 후 이동
- **git branch** : branch 목록 확인
- **git branch -d (branch name)** : branch 삭제
- **git merge (branch name)** : 현재 branch에서 병합한다.
- **git log --graph** : log를 그래프로 본여준다.
- **git log --graph --oneline** : log 그래프를 한줄로 간략하게 보여준다.

[merge와 pull 강의자료](https://aidenlim-edu.github.io/class-git-advanced)



# PR(Pull Request) 사용하기

collaborator인 사람이 새로운 브랜치를 만들어서 master 브랜치에 직접 push하는것 보다 master에게 PR을 보내고 master가 push하는 경우가 실제 업무의 대부분



**PR보내는 법** : 

repo를 clone -> branch 생성 -> 변경사항 반영 -> 생성한 branch push -> github repo에서 PR작성

-> master가 확인후 merge





# fork

**clone** : 다른사람의 remote repo -> 내 local 

**fork** : 다른사람의 remote repo -> 내 remote repo



**fork 하는 법** : 

상대방의 github repo에서 우측 상단의 fork 클릭 -> 나의 repo에 복사되면 clone으로 내 local에 연결

-> 내 repo에서 PR을 보냄 -> 나에게 PR 수락의 권한이 없음



# HEAD

공부하기

