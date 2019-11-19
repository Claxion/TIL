

| Vue.js              | Django |
| ------------------- | ------ |
| Vue router<br />JWT | DRF    |



2개의 프로젝트가 필요함 - 각각 front, back 으로 구분해보자.

js 만으로 할 때는 back 단에 express 를 쓸 수도 있다(node)



vue ui 를 해당 폴더에서 친다 - 프로젝트 폴더 불러오기 -> gui로 만들 수 있음

왜 vue router를 쓰느냐 : 

일반적인 spa의 단점 -> 

(1) 페이지 내부에서 어떻게 움직였는지 추적이 안 된다.(히스토리 관리가 안됨)

브라우저에서 window.history.back () 되돌아가기 : spa 쓰면 이게 안 됨

(2) SEO 에 취약. search engine optimization 검색 엔진 최적화

 html 페이지가 가지고 있는 컨텐츠를 통해서 결정됨. 매우 중요함. 이탈율과 유입율

spa는 html 요소가 거의 없음. js를 통해서 나중에 렌더되기 때문에.. 요즘에는 많이 해결됨.

ex) hashbang (#!) <- 히스토리 안에 저장되는 요소

-> js로 라우팅을 할 수 있도록 하자

(우리가 보는 화면은 검색엔진의 스파이더들로 모아놓은 자료들을 보는 것 - 리얼타임일 수는 없다. 갓구글의 페이지랭크 시스템. 최근에는 페이지들의 영향력을 평가해서 올려두기도 한다.)



vue ui 에서 플러그인에서 추가하고 나면, vue add router

그러면 use history mode for router ? 물어보면 yes



js는 export default 로 필요한 만큼을 내보내줄 수 있다. 다른데서 쓰려면 명시해야함.

Auth 와 Todo 두 개로 구성하자.



router link는 링크를 만들어준다. (페이지 로드를 없애기 위해 - 클릭 이벤트가 없어짐 a태그로 달면 이벤트가 발생)

router-view는 각 router에서 사용하는 양식을 렌더링한다.



vue에서는 vuetify를 많이 사용



noscript tag : javascript가 enable 되지 않았을 경우 뜨는 것

bootstrap을 쓸 때는 css만 임포트해서 써야 충돌 우려가 없음.

주소에서 @는 src 의 대체어 

vue.js에서는 form 태그 안 쓸 예정



프론트와 백을 서로 다른 깃을 이용해서 작업해보자. 협업을 한다고 생각해보고 가상환경 만들어두고 사용

python -m venv (이름)

source (이름)/Scripts/activate

.gitignore 로 venv 생략 + django 기본을 gitignore 검색해서 정리

$ pip install djangorestframework

https://www.django-rest-framework.org/tutorial/quickstart/#settings

$ pip install djangorestframework-jwt

https://jpadilla.github.io/django-rest-framework-jwt/

$ pip install django-cors-headers

https://github.com/adamchainz/django-cors-headers



cors, jwt, restframework 모두 settings에 추가

jwt_auth , rest_framework 들을 복붙

cors 관련 middleware 추가

cors - configuration 에 접근을 허용할 것을 넣어놔야한다. 

front domain host 를 whitelist에 넣어두고 거기서만 받는다.



장고의 세션

http -> stateless 인것을 해결해서 stateful. cookie 베이스.

장점: 매우 빠름

단점 :  매우 많은 사람이 접속하면 그 정보를 모두 저장해야함. 여러 디바이스로 접속 가능. 멀티 디바이스에서 공유가 불가능함.



--------

jwt 은 인증되었다는 정보를 서버는 저장하지 않고, 그 정보를 프론트에서 전달함. 세션을 조회하지 않고, 토큰으로 조회.  토큰의 보안을 위해서 암호화 과정을 진행. stateless

https://velopert.com/2350

jwt.io // AuthO



형식 : xxxx.yyyy.zzzz



vue session을 이용해 관리할 것



// 이제 뷰에서 로그인이 되면 -> 로그인을 할 때 장고 서버로 보내서 token 을 만들어낸다. 

// 뷰 세션으로 관리하자.

npm i vue-session



main.js 에서 Vue session  import & Vue.use(Vuesession)

vue-session npm 기초함수들 익히기



life cycle ..

sessionkey이 한 번이라도 만들어져 있으면, 체크해주는 것. <- 뷰가 생성되기 전에 key를 확인하고 싶다.

vue의 라이프사이클을 이해하자

created, mounted, updated, destroyed 4가지의 전후의 포인트를 잡지만 보통 mounted 직전에서 많이 다룬다. 이 지점에 훅을 달 수 있다. 

유저가 이미 로그인을 한 것인지 확인 필요



POSTMAn으로 테스트할 때는 JWT (spacebar) jwt_key 를 headers에 추가해서 보내준다.