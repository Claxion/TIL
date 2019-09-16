명세

Board Template CRUD

1. project Board -> app posts	
2. Model Post

- title
- content
- created_at & updated_at



2. url

- /create
- /detail/1
- /index
- /update/1
- /delete/1





댓글도 게시글과 똑같지만 , 내용만 들어간다고 생각하면 된다.

댓글은 게시글에 속한 애들

여러 종류의 클래스를 저장한 테이블들은 서로 간의 여러 관계를 가지고 있을 것임

4가지 관계 : 

0. 관계없음 
1. 1:1 : 다른 테이블의 레코드가 하나씩만 연동되어 있는 경우
2. 1:N : one to many, many to one 대부분이 해당됨, 1 has many, n belongs to 1
3. N:N : many to many



사실은 하나의 컬럼을 추가하는 것으로 정보를 쉽게 테이블에 추가할 수 있음.

그러나 여러 종류의 정보는 계속적으로 추가될 수가 있음. 데이터들이 중복일 수 있다.

여러 테이블들의 관계를 만들어줌으로 중복을 해소하고, 변경시의 문제들을 처리하자.

유니크한 id들을 가지고 정보들의 관계를 표현할 수 있다.

1:다에서 많은 쪽에서 자기가 속한 정보를 가지고 있다면 훨씬 편리하게 접근가능

주로 N쪽에서 1의 정보를 가진다. 외부를 참조하는 FK(foreign key)

fk장고는 자동으로 만들어주는 기능을 지원한다.

1과 n에서 각각 서로에게 어떻게 접근하는가? 

