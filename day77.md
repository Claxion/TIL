장고 쿼리셋  exists 유용하다. for문 돌면서 찾는것보다 

get은 값이 없으면 에러가 발생하고 filter는 빈 쿼리셋이 나와서 filter를 더 많이 쓴다. 

get은 WHERE LIMIT 1의 느낌이고 filter는 WHERE의 느낌.



캐싱을 지원하는 dtl 문법 <- db 접근 최적화  (with template tag로 검색)

{% with total=business.employes.count %}

 {{total }} employee {{  total|pluralize }}

{% endwith %}



{% with a=1 b=2 %}

{% endwith %}



이렇게 하는게 미리 정의된 결과물을 ctx로 전달하는 거랑 큰 차이는 없음



1:1은 칼럼으로 들어가도 될 친구들을 독립성을 유지하기 위해서, 따로 테이블로 분리한 것이라 생각하면 좋다.



AbstractUser : user의 기본적인 요소들

AbstractBaseUser: password 가짐

기본 세팅은 conf 의 global_Settings.py 에 있음

모델 관계에서 related_name은 역으로 접근가능한 이름을 얘기한다.



쿼리셋을 컨트롤하기

make query!

쿼리셋은 합쳐져도 쿼리셋이어야함.



instagram tech blog -> the world's largest django app



orm 의 장단점이 뭐냐 ? 

lazyloading 이 뭔지 아니

장고는 사용자가 잘 모를 것을 전제로 하고, 막 호출을 하더라도 정말 필요할 때만 한다.

따라서 with은 잘 사용하지 않는다.

도널드 커누스