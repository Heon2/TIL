# Unix/Linux 명령어

- **파일로 이동** : cd (파일명)

- **상위파일로 이동** : cd ..

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
- **git commit -m "수정하고 싶은 이름"** : commit을 하고 commit 이름이 "수정하고 싶은 파일"로 저장된다.
- **git config --global user.email** : 깃허브의 이메일 주소를 입력한다.
- **git config --global user.name** : 깃허브의 user name을 입력한다.
- **git remote add origin (remote_repo_url)** : remote repo를 local로 복사합니다.
- **git push -u origin master** : 처음 연결을 할때 계정에 로그인하기위한 명령어
- **git push origin master** : local repo의 최신 커밋을 remote repo로 push합니다.
- **git clone (remote_repo_url)** : remote repo를 내 local에 복사합니다.