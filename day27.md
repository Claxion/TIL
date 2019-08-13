결제 모듈  : 아임포트

# django

여러 가지로 중첩이 발생함.

DRY : do not repeat yourself



네브바는 모든 페이지에 존재해야함...복붙?? => 주로 템플릿 상속으로 처리함 

1. 공통적으로 쓸 템플릿(코드)을 뽑아낸다.
2. 해당 파일을 따로 만들고, 
3. 활용할 다른 템플릿 파일에서 불러와 쓴다. extends => 를 쓰는 경우에는 전체를 바꾸게 됨
4. 다른 곳에서 사용할 부분은 {% block body%} {% endblock %}처리를 해놓음
5. 사용할 곳에서는 컨텐츠만 남겨놓고 다 지운다. body, html, h1 등의 태그를 다 지움



partialview의 경우에는 _ 붙이는게 convention ,.

_nav, _footer 등

그냥 partial로 넣을 때는 extends가 아니라 include를 사용한다.



artii :: ascii art api

1. 사용자 입력을 받아 artii API ascii art 를 보여주는 앱 
2. 입력은 /artii/
3. 출력은 /artii/result



alias 적용 source ~/.bashrc

string 만 넘겨주게 되면, 그냥 표현해주지만, html 요소가 하나라도 들어오게 되면 알아서 html 요소로 해석해서 돌려주기도 한다. 그래서 pre 로 처리할 필요가 있음.



여전히 불편한 점이 있다. 좀 더 장고스럽게 쓰는 방법? 

여러 앱을 사용할 때, urlpattern에 계속 추가해야되나? 여러개의 분리해놓은 템플릿 상속을 다른 앱에서 사용할 수 없는듯하다 어떻게 해결하지? 

문지기 urls를 여러 문지기들로 분리해야한다.
상위의 template들을 구축한다.

완전 공통으로 쓰일 템플릿들은 완전 공통 레벨로 분리해낸다.

프로젝트 메인 폴더에 templates 를 만들어서 옮김

redner에서 파일명을 어떻게 찾는가? 

해당 앱에서 templates에서 검색하고 ...다른 앱에 있는 templates를 검색한다. 벗 프로젝트 메인 폴더 templates는 검색하지 않는다.

그러면 Project 메인 폴더의 =->tempaltes->'dirs'

경로 설정시에는 파이썬이 만들게끔 한다. 장고에는 BASE_DIR로 기본 프로젝트 절대경로가 상수로 정의되어 있음

이때 os 모듈을 사용함. 여러 종류의 os에 맞춰서 각종 경로와 스트럭쳐를 처리해줌

``` python
current = os.getcwd() #: 현재 폴더의 경로
os.path.join(current,'templates') # 콤마로 구분된 것을 알아서 뒤에 붙여줌
```

사실상 모든 templates 폴더를 장고가 다 찾기 때문에 문제는 없음. 관리의 용이함 때문에 사용하는 방식

같은 이름을 가진 중복된 템플릿 html 들이 있을 가능성이 있음. 이 경우에 템플릿 호출시 혼동이 일어날 가능성이 있음

이것을 해결하기 위해서 templates->artii 안에서 배치할 수 있다.

