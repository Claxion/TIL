scrimba 코딩 플랫폼?

장고는 파이썬의 특성을 온전히 다 사용할 수 없음(html)

데이터를 저장해보자.

튜플->리스트->딕셔너리->클래스~

article 클래스 : title, content, created-at



dbms수정, 삭제 등이 매우 빠르고 간편함.

amz redshift

70년대부터 rdbms 지금은 달라짐.

관계형 db  : ex) excel

mysql, sqlite, postgresql, orm 등등

핀테크 업체들은 굳이 oracle에 의존하지 않는 경우들도 많아짐



스키마: 데이터베이스의 메타데이터? 어떤 데이터를 관리하는지 알려줌.

행과 열로 이루어진 데이터 요소들의 집합. 

.어떤 요소들이 들어오는지와 데이터 형식이 지정됨

PK(기본키): 각 행 또는 레코드의 고유값. primary key. id

엑셀 시트 : 테이블



SQL : RDBMS의 데이터를 관리하기 위해 설계된 특수 목적의 프로그래밍 언어임. 자료 검색과 관리. 디비 스키마 생성과 수성, 객체 접근 조정 관리 가능

CRUD

Select : read, insert into : create , update : update , delete : delete



ORM이라는 놈은 파이썬의 객체를 다루듯이 SQL을 다룰 수 있게 해준다. 파이썬 코드로 조작가능함.

디비를 직접 다루기보다는 ORM을 통해서 많이 다룸. SQL을 직접 쓰는 것보다 ORM을 쓰는 것이 더 빠르고 정확함.

DB의 행이나 테이블도 객체로 취급해보자. ex) django orm



python manage.py (runserver, startapp ,makemigrations)

makemigrations : 장고가 진행해줌. 클래스의 상세 설계도를 자동으로 만들어준다.

실제 db에 적용하는 과정이 migrate.

model을 변경하고, 이 변경된 모델을 makemigrations을 통해서 sql 관련된 형태로 변형, 그리고 이것을 migrate 를 통해서 db에 적용한다.

sqlite3 검색후 sqlite install

설계도를 변경한 경우 위를 다시 반복한다. 이 때 옵션이 있음. 1) 한번만 사용될 값을 추가해주거나, 2) 그만두거나 

원래 있던 데이터를 어떻게 다룰거냐? 기존의 데이터가 있다면 1) default 값으로 null 값을 넣어준다.

sqlmigrate articles 0001 실제로 어떻게 만들어진건지 sql 구문으로 보여줌

직접 db 다루는 shell을 열 수도 있음.

python manage.py shell

``` python
from articles.models import Article
Article.objects.all() # 모든 article 객체를 다 가져옴 query set을 돌려줌
#객체를 만들고 값을 추가하는 방법
article = Article() # article 객체 선언
article.title = "" # article 객체의 어트리뷰트데이터 추가
article.content = ""
article.save() #저장
Article.objects.all() 
len(Article.objects.all()) # 리스트와 유사
Article.objects.all()[0] # index 접근 가능 단, 음수 인덱스는 지원안함
first_article = Article.objects.first() # 선언도 가능
first_article.title 
first_article.image_url
first_article.created_at # 아까 만드는 시점에 세팅됨
# 생성자를 이용하는 방법
article_two = Article(title='second',content='this is from generator')
```

실제로 1.0.0 release 된 이후에는 가능한 한 모든 정보를 추적할 수 있도록 migration 정보를 남기는 것이 좋음

아닌 경우에는 그냥 자유롭게 변경해도 상관없음

db를 날려주고 싶을때는 db.sqlite3 파일만 날려주면 된다.



### admin

python manage.py createsuperuser

id, email, pwd  1234 ,~,1234

admin에서 article을 보기 위해서는 등록을 해줘야함.

admin.site.register(Article)

