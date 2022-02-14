리모트 저장소란? 깃허브 사이트.
로컬 저장소란? 내 컴퓨터.

Git의 Repository 구조는 크게 세 가지로 구성되어 있다.
작업트리(Working Directory) > 인덱스(Staging Area) > 저장소(Head Repository).
우리가 작업하는 폴더를 작업트리(Working Directory)라고 부르며 commit을 실행하기 전에 작업트리와 저장소 사이에 존재하는 가상의 준비 영역(Staging Area)를 인덱스(Index)라고 한다.
저장소에 commit을 하기 위해서 먼저 추가(Untracked Files) 및 변경(Modified Files) 하고자 하는 파일을 먼저 인덱스에 기록(Stage)하고 이후 스테이징된 목록만 최종적으로 commit 명령어에 의해 저장소에 공개하게 된다.
작업트리(Working Directory) >add> 인덱스(Staging Area) >commit> 저장소(Head Repository).

- - -
트러블 슈팅
error:failed to push some refs to
git push를 했을 때 위와 같이 에러가 발생하는 경우가 있다.
이는 리모트 저장소에 내 로컬 저장소에는 없는 파일이 있을 때 내 파일을 push하면 발생하는 오류이다.
이럴 때에는 내 로컬 저장소에는 없는 그리고 리모트 저장소에는 있는 그 파일을 pull한 후 리모트 저장소에 다시 push를 해야한다.
- - -
명령어 정리
- - -
최초 한 번만 하면 되는 것
git config --global user.name <yourName>
git config --global user.email <yourEmail>
git config --global core.autocrlf true: 이 명령어를 통해 CRLF를 LF문자로 변환할 수 있다.
- - -
그 외
--help를 붙이면 그 명령어에 대한 헬프창이 나온다. 예) git remote --help
git clone: 리모트 저장소 주소: 로컬 저장소에 리모트 저장소의 모든 것들을 가져온다.
git status: 변경 사항을 체크한다.
git add
git commit -m ""
git push
git remote -v: 현재 로컬 저장소와 연결된 리모트 저장소를 조회한다.
git log: 커밋 내역을 조회한다. (END) 표시가 사라지지 않을 시에는 "q"를 눌러주면 된다.
git log -p: 단순히 커밋 내역을 조회하는 것이 아니라 어디 부분이 추가되고 수정되었는지 출력해준다.
git add <대상>: 대상을 인덱스에 기록한다.
git commit -m "": 리모트 저장소에 올리기 전 최종상태로 만든다.
git push: commit된 것들을 리모트 저장소에 올린다.
git pull <리모트 저장소의 별칭 보통은 origin> master: 리모트 저장소의 파일 중 로컬 저장소에 없는 것들을 로컬 저장소로 옮긴다.
git reset HEAD <file>: 이 명령어를 통해 git add를 취소할 수 있다. git reset만 친다면 add한 파일 전체를 취소한다.
git remote remove origin: 이 명령어는 연결된 리모트 저장소를 연결을 해제할 수 있다.