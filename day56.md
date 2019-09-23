https://www.youtube.com/watch?v=V5hZoJ6uK-s

MIT 6.046J introduction to algorithms 2005 fall



웹 DB

장고가 데이터를 관리 ORM을 이용했음.

Django(ORM) -> Databae(DBMS)  , sql



berkeley database 구글 검색 / CS186 디비를 만드는 수업



python manage.py shell_plus

var.query : 실제로 사용되는 쿼리문



왜 파일 대신 DB를 사용하느냐??? - 체계화된 데이터의 모임



https://www.sqlite.org/download.html

precompiled binaries for windows

64 dll & bundle of command line

home folder에 sqlite 폴더 생성 후 다운받은걸 배치함 (파일5개)

환경변수 path에 추가

git에서 (git은 cygwin, min, cmd, winpty 등등 다양한 환경을 쓰고 있음)

winpty sqlite3로 실행



alias 세팅후 sqlite3 db.sqlite3로 접근가능

### sql문법

.exit 

.databases

.tables 

 (장고를 통해서 만들면 테이블명이 app이름_class이름)

SELECT * FROM posts_post;

SELECT title FROM posts_post;(FROM 에 항상 테이블명 사용할 것)

db열기 : sqlite3 (없어도 생성해서 열어준다)

.databases를 이용해서 파일을 만들 수 있음..(저 용도로만 쓰나?)

.mode csv (csv input 모드)

.import CSV table명

.headers on (헤더 추가)

.mode column(칼럼 모드. 예쁘게 보여줌)



만들기

CREATE TABLE table명(

column1 INTERGER PRIMARYKEY,

column2 TEXT

);

타입들

INTEGER, TEXT, REAL, NUMERIC, BLOB(주로 바이너리 파일)

.schema table명 : 어떤 컬럼들로 구성되어있는지 보여줌

날리기

DROP TABLE table명

추가

INSERT INTO table명 (column1~) VALUES(value1)

전체를 다 넣을 때는 컬럼명 생략 가능

PRIMARY KEY를 이용해서 중복 입력 방지할 수 있음

빈 입력을 방지하기 위해서 NOT NULL 사용



가능하면 rowid를 그냥 쓰는 것이 좋음.

그러나 sql이 아니라 다른데랑 같이 쓸때는 따로 선언해주는 것이 좋음

가능하면 DB에서는 null을 허용하지 않는 것이 좋다



SELECt 시에 Limit을 쓰면 원하는 양만큼 가능

Limit 2 

Limit 2 offset 2; (offset은 리밋과 무조건 같이) offset만큼 띄우고 그 뒤부터

-> 게시판 페이지 등..



조건 조회

WHERE column=value;

중복없이 

SELECT DISTINCT



primary key의 autoincrement는 무조건 사용해야

변경 

UPDATE 클래스이름 SET name='~' WHERE id=?

여러개도 바뀜



이미 있는 클래스에다 import를 하게 되면 맞춰서 넣을 수 있다(스키마에 맞게 넣을 때는 header exclusion 해야된다) - sqlite3는 해당 옵션이 없음..

전체 개수 세기 SELECT COUNT(*) FROM users

integer 형으로 바꿀 수 있는 것들은 avg, sum, min, max 모두 사용가능



Like 와일드카드 패턴

_ : 반드시 이 자리에 문자가 존재해야

% : 이 자리에 문자열이 있을수도 없을수도



ORDER 정렬

ORDER BY  ~~ ASC|DESC

여러 개의 칼럼이면 순서대로~



테이블명 변경

ALTER TABLE exist_table RENAME TO new_table;

칼럼 추가

ALTER TABLE table ADD COLUMN col_name DATATYPE;

NOT NULL 조건을 빼거나 DEFAULT 조건 추가

ALTER TABLE news ADD COLUMN subtitle TEXT NOT NULL DEFAULT 1;