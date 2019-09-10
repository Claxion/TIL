깃의 브랜칭을 간단하게 배울 수 있는 사이트

https://learngitbranching.js.org/



* 깃 리베이스



unstage

git rm --cached -r .   전부 언스테이지



pull request



fork : 나의 깃헙으로 가져오는 것

clone: 로컬에 가져오는 것



github 상에서의 pull request : fork 를 가지고 이용하자. 나는 내가 fork 한 것에 대한 권한이 있기 때문. 

이것을 pull request를 요청하면 오너가 해당 내용을 반영하는 시스템

owner는 merge pull request를 진행한다.

create a merge commit /squash and merge / rebase and merge 등의 옵션이 있다. 



pull : fetch + merge

원본에 변경이 일어났다면

1. 포크를 새로 떠서 클론받기
2. 원본을 가져와서 그걸 fetch가 되도록 추가를 한다.
   git remote add upstream
3. 그럼 관리되는 remote가 두개가 된다.
4. git fetch upstream
5. git merge upstream/master
6. 다시 주루룩