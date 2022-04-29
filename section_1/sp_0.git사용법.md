git status 명령어를 통해 staging area와 untracked files 목록에 어떤 것들이 있는지 확인할 수 있습니다.

git restore <파일 명>
commit 되지 않은 Local Repository의 변경사항을 취소 할 수 있음

git add <파일명>
내 Local의 untracked file을 Git의 관리 하인 staging area로 추가할 수 있습니다.

gi add.
Staging area에 모든 파일을 한번에 추가할 수 있음.

git commit(나의 Origin Repository에 업로드 하기 전 단계) 

git commit -m '커밋 메세지'
-m 옵션을 통해 커밋할 내용의 코멘트를 작성할 수 있음

git reset HEAD^
아직 Remote Repository에 올라가지 않은 commit 이면
reset 명령어로 취소할 수 있습니다.

$ git reset --soft HEAD^ (going back to the commit before HEAD) 
$ git reset --soft HEAD~1 (equivalent to "^") 
$ git reset --soft HEAD~2 (going back two commits before HEAD)



HEAD는 연속된 ^의 shortcut 입니다. 예를 들어 HEAD3은 HEAD^^^와 같습니다. 
즉 이 상황에서는 HEAD~1 명령어도 가능합니다.

추가적으로 hard, soft 옵션도 있는데 reset 에 
대해서 더 공부하고 싶으시다면 git reset --hard vs --soft 등의 
검색어로 구글링 한 후 실습해 보시는 것을 추천드립니다.

git push <origin><branch>
리모트에 있는 origin의 master 브랜지에
Local Repository의 변경 사항을 업로드하기 위해서는
git push origin master라고 입력

git log
현재까지 commit한 내역들을 터미널 창에서 확인
(빠져나오기는 q를 입력)



함깨 작업

git init
디렉토리를 git Repository로 변환하거나
새로운 Repository를 초기화하는데 사용
내 컴퓨터에서 내가 직접 만든 디렉토리를 
Git의 관리 하에 들어가게 만들어 주는 명령어는 git init 입니다. 

git remote add origin <Repository 주소>
Local Repository에 Remote Repository연결

git remote add pair <pair의 Repository 주소>
pair의 Remote Repository에 연결

git remote -v
현재의 Local Repository와 연결된
모든 Remote Repository 목록 확인

git pull <shortname><branch>
Remote Repository의 해당 branch내용을 Local Repository로 가져옴



git branch main 말고 다른 branch 에서 clone 받는 방법 

git clone -b {원하는 branch명} --single-branch {clone 받을 git 주소}


Git에 만들어져 있는 branch이긴 한데

local에 다운로드 받지 않았을 경우

 

git switch branch명으로 branch 변경이 되지 않는데

$ git switch branch명
fatal: invalid reference: branch명

이런 식의 에러가 뜨게 된다

 

여기서 변경을 해 주려면

git pull 으로 신규 branch를 받아준 뒤

git switch branch명 을 사용해주면 된다

## 원하는 위치에 잔디 심고 싶을 때.
git commit --amend --no-edit --date "Fri 15 Apr 2022 14:00:19 KST"