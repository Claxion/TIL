basecamp

프레임워크의 규칙들을 따라야하나?

# django

패턴 MVC ,MVVM  ..등

MVC가 웹서비스에는 가장 적절하다고 인정받고 있음 

장고에서는 MTV라고 이름붙임.

M : 데이터 관리 

 T : 사용자가 보는 화면

V : 중간관리자(제일 중요..) ->M,T를 관리함

start command

django-admin startproject first_app

프로젝트 네임 컨벤션

대문자 프로젝트 명 안에서 장고를 생성하는 것으로 하자

python manage.py runserver 로 실행

<hr>

프로젝트 안에서 각 앱들이 들어온다.

python manage.py startapp pages

admin.py 관리

apps.py 앱관련 config들

views.py View

models.py Model

장고에서는 트레일링 컴마 컨벤션을 사용함. 

list = [
a ,
b,
] 

unable to import django => f1 select interpreter 인 가상환경

urls.py 의 urlpatterns에 추가한다.

views.py의 함수는 무조건 http.response라는 객체를 돌려줘야 한다.

ctrl+p => urls.py 바로 쳐서 움직이자

여러 문지기들을 관리할 수 있음 => 앱 안에 url 관리하는 문지기들을 처리할 수 있음

csrf 토큰으로 보낭ㄴ처리



## python

list를 key로 sort 하기

``` python
def take4(elem):
    return elem[3]

list.sort(reverse=True, key=take4)
```

 튜플안에 리스트를 넣어서 작은 클래스 형태로 쓰면서 데이터를 변경시킬 수 있다.



