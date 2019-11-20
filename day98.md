만들고 있는 시스템의 구조

App.vue -> router ->  Home.vue , Login.vue

Home.vue -> TodoInput.vue, TodoList.vue

Login.vue



vuejs 의 프론트단에서, jwt 의 토큰을 디코딩해야함.

jwt 디코딩은 npm i jwt-decode 로 패키지를 깔고 사용한다.

get 을 할 때는 jwt 을 같이 실어서 header에 포함시켜줘야한다.



form @submit 을 이용해서 엔터와 클릭 두 이벤트를 동시에 처리할 수 있다. 

원래는 form 이 데이터를 보내주는 것을 하는데 거기에 prevent를 달아서 그 기능을 막고 사용할 수 있다. 

ex @submit.prevent="function"



백서버는 하나로 웹+모바일 프론트를 동시에 처리할 수 있다. 

장고 단일로 구성하는 것보다 확장성이 있다.

