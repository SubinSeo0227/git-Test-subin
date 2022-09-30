# git-Test-subin
배고파여


1.https://git-scm.com/book/ko/v2
2.https://backlog.com/git-tutorial/kr/

Git
-Terminal(window+R > cmd) vs GUI(클릭해서 타고 들어감) :속도의 차이 전체적인 조감도 볼 수 있는 장점

INSTALLATION
:터미널
git>downloads>setup다운>Choosing the default deitor used by Git(Use Visual Studio Code as Git's default editor) > Visual Studio Code >우측상단 다운로드 >zip다운로드 > 압축풀고 비쥬얼스튜디오 열고 >나머지 깃 다운로드 진행> 맨마지막창에 위에거 체크 아래꺼 언체크 >1사진대로


:GUI
https://www.gitkraken.com/download/windows64 >다운로드 > 구글로 로그인 > 돈내지말고 넘어감> 깃터미널에 pwd부터> 

비쥬얼스튜디오 폴더 불러오기> datatype.txt만들기>

git --version:버전확인
git config user.name:이름확인
git config --global user.name"subin": 이름설정
git config user.email:이메일확인
git config --global user.email ssb~~~:이메일 설정
pwd: 파일위치확인
mkdir MyFirstGit: 디렉토리생성
cd MyFirstGit: 디렉토리 진입
git init:이제부터 여기는 모든걸 볼거야!
git add ~txt: 파일추가(띄어쓰기 후 쓰면 한번에 두개 추가 가능)
git status: 파일상태확인
dir:내용보기
dir -a:안에 있는 디렉토리 다 보여줘
cd .git: .git으로 갈래!
cd ..:다시 한단계 뒤로 나갈게
touch outline.txt: outline.txt하나 만들어줘
git add - :없는 파일 보내줄게!추가할게!
rm -r 폴더이름: 삭제하기
git commit -m: 메세지를 커밋하겠다
git log: 무엇을 했는지 기록을 알 수 있음
======================================
9/27일

-git add .:전체를 추가 (모든 파일수정이나 추가해야할 경우)
-code .: 코드 바로 띄우기
-git add 새로만든폴더/파일명: 새로만든 폴더안의 파일 추가 (새로 만들어진 폴더는 폴더명/로 뜸)

-commit 추가
git commit → Vim → i 누르면 INSERT가 됨 → 한줄추가하고 esc → :wq(Vim나가기)
-git commit --amend: 코멘트수정

-git log --oneline: 코멘트만 한줄로 쫘아아악보여줌
-touch .gitignore:init으로 통제는 받지만 보여주기 싫은것이 있을때
파일을 만들고 생성된.gitignore에 파일이름을 치면 활성화되지 않는 회색으로 글자색변함

------
수정이나 추가 한 후 commit하기 
-----
새로운 폴더 만들기
(master)-원본
(branch)-복사본 
원본은 두고 복사본을 수정한 후 채택되면 원본에 옮김
-On branch master - 가지치기없이 쭉했음

git branch alba1: alba1이라는 branch생성
git branch: 어떤 branch가 생성되어 있는지 확인
git switch alba1: alba1으로 가겠다 → 하고나면 (master부분이 alba1으로 바뀜)

alba1에서 수정후 master로 가면 master에서는 수정전이 보임. 싱기방기

git branch로 수시로 내가 어느위치에 있는지 확인.

git commit -a -m:추가와 메세지를 한번에

========================================
9/28
merge=합병

-git switch -c: branch만들기와 만든 branch로 접속이 동시에 이루어짐.
-cat 파일명: 파일 안의 내용볼 수 있음.
-git checkout master: switch랑 같은역할.
	(git checkout -c는 안돼! -c는 switch에서만 먹혀!) 
-
1.pizza branch 생성 후 pizza파일 생성  
2.새로운 파일을 만든 후 처리를 안하고 넘어가면 git commit -a -m 이 안먹힘. 따로따로 하나씩 해줘야 함.

-git branch -d ~:branch삭제 (자기자신은 삭제 불가 , master에서 관리)
-git branch -m : branch이름 바꿈(바꿀 이름으로 들어가야함)
-git branch -D ~:branch삭제
-
-git merge 이름:메인보다 더 좋은것이 있을 때 메인으로 바꿈.
-git merge --quit : merge 오류날때 치고 확인

==============================
9/29
-(repository 를 만들어라 하면 저장(공유)할 파일하나 만들란소리)
-새로 만들어진파일은 git commit -a -m 이 안돼. 하나씩해야함.(git add . → git commit -m 으로)
------------------------------
-.gitignore는 깃이 설정해둔 명령이기때문에 파일명을 바꾸면 내용숨기기를 할 수 없음! 
----------------------------
-merge에 오류 나면 git merge --quit치고 코드내용 넣을거 넣고 수정 후 add후 commit 하기 
------------------------------
-git checkout 6f2b0f6 : 복구하고 싶을때 git log --oneline 앞의 숫자 복사
다시 돌아올땐 master로 돌아가면 돼.
오류로 인해 문제파악이 필요할때 씀 


