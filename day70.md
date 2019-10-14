DRY : 재사용성

Form -> model Form -> Auth  + M:N + validation(TDD)

-> Deploy + Javascript



- Google Maps를 최초에 자바스크립트 만으로 구현하면서 모바일라인에서 어도비를 구축
- Apple도 거절



자바스크립트 프레임워크들이 나오기 시작 

Ember 나 Backbone 등이 너무 무겁고 사장되기 시작해서 -> Angular(google), React(Facebook),Vue 등으로 옮겨감

1대장은 React이고, Vue는 심플하기 때문에 빠르게 올라오는 중

i18n : 국제화 작업(internationalization)

l10n : 지역화 작업(localization)



TDD : test driven develop



restfulAPI

장고는 put, delete 들을 지원하지 안하서 restful하게 짜기는 힘들다.

put, delete는 자바스크립트가 지원하고 기본 html5는 지원하지 않는다. 이러한 rest 규칙을 지킨 페이지들을 restful api라고 한다.



django-rest-framework라는 놈으로 장고에서도 처리할 수 있다.



텀블벅 (프로젝트 크라우드 펀딩 사이트)



작업중 로그인을 하려면 그 정보를 가지고 있어야한다. next=/admin/ 등으로  그 정보를 기록해둔다 혹은 어디서 왔는지 추적하기도 함.



graphQL(facebook이 만든 쿼리언어)

github이 공식적으로 지원



장고의 모듈화된 폼

html 버전에서 구축한 form -> django Form class -> model Form



장고 부트스트랩4

단순히 만드는데서 국한되는 것이 아니라, 더 많은 기능을 사용할 수 있음

authO 라는 사이트