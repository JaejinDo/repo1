리모트 저장소란? 깃허브 사이트.
로컬 저장소란? 내 컴퓨터.

Git의 Repository 구조는 크게 세 가지로 구성되어 있다.
작업트리(Working Directory) > 인덱스(Staging Area) > 저장소(Head Repository).
우리가 작업하는 폴더를 작업트리(Working Directory)라고 부르며 commit을 실행하기 전에 작업트리와 저장소 사이에 존재하는 가상의 준비 영역(Staging Area)를 인덱스(Index)라고 한다.
저장소에 commit을 하기 위해서 먼저 추가(Untracked Files) 및 변경(Modified Files) 하고자 하는 파일을 먼저 인덱스에 기록(Stage)하고 이후 스테이징된 목록만 최종적으로 commit 명령어에 의해 저장소에 공개하게 된다.
작업트리(Working Directory) >add> 인덱스(Staging Area) >commit> 저장소(Head Repository).

명령어 정리
- - -
최초 한 번만 하면 되는 것
git config --global user.name <yourName>
git config --global user.email <yourEmail>
- - -
그 외
--help를 붙이면 그 명령어에 대한 헬프창이 나온다. 예) git remote --help
git clone: 리모트 저장소 주소: 로컬 저장소에 리모트 저장소의 모든 것들을 가져온다.
git status: 변경 사항을 체크한다.
<<<<<<< HEAD
git add
git commit -m ""
git push
git remote -v: 현재 로컬 저장소와 연결된 리모트 저장소를 조회한다.
=======

git log: 커밋 내역을 조회한다. (END) 표시가 사라지지 않을 시에는 "q"를 눌러주면 된다.
git log -p: 단순히 커밋 내역을 조회하는 것이 아니라 어디 부분이 추가되고 수정되었는지 출력해준다.

git add <대상>: 대상을 인덱스에 기록한다.
git commit -m "": 리모트 저장소에 올리기 전 최종상태로 만든다.
git push: commit된 것들을 리모트 저장소에 올린다.
>>>>>>> a31010da0e2960833a855a23ae5b03fef8fbe941
