vue router

vuex : 데이터를 전체적으로 관리하는 덩어리

server와 front를 각각의 서버로 구축 

django-server , vue-server 독자로

json web token (jwt)



heroku, aws , docker  를 이용한 배포



각각의 vue component에 먹일 수 있는 css를 제한시켜놓을 수 있음(style 태그에 scoped)



부모 컴포넌트에 scoped를 쓰게 되면 그것을 물려받는 아이들에게도 다 적용된다. (이름이 같다면)

그래서 구분을 해주는 것이 좋다. vue 컴포넌트별로 스타일을 다르게 먹일 수 있다는 장점이 있음



data를 함수화 된 이유: 자기 것만을 들고 있고 싶어서