app 밑에 component를 구성한다.

data를 function에게 넣는다. 

props? : 원래 컴포넌트가 데이터를 쓰려면 집주인이 props의 형태로 공간을 만들어줘야 가능하다.

하나의 html로 만들기에는 양이 많아지기 시작

장고는 기본적으로 분리해줘서 보기가 편했었음. vue의 코드도 그런 식으로 쪼개보자.

싱글 컴포넌트->멀티 컴포넌트 -> Single file component pattern 사용

한 컴포넌트는 하나의 파일에. 확장자는 .vue

자바스크립트는 파일을 여러 개 썼을 때 데이터를 공유하기가 좀 힘듦. 

webpack이 이런 역할을 쉽게 해 줌. 그것도 까다로움..

vue-cli 로 커맨드라인으로 시작을 할 수 있게 해줌

갓갓 npm

패키지 관리를 어떻게 하는가?

파이썬의 경우에는 전역으로 전부다 패키지를 깔게 됨. 그래서 때로는 불편하고 venv를 만듦

npm은 프로젝트별 패키지 관리가 가능하다. npm 은 전역과 프로젝트 단위를 선택해서 설치할 수 있다. (글로벌, 로컬or project ) 디폴트가 프로젝트 단위임. 글로벌은 npm install --global 이라 해야함

npm install -g 로 약어

페이스북이 yarn을 만들었는데 , npm에 yarn의 좋은 점을 다 반영하게 됨.



vue create projectname

please pick a preset default ...



### 번외

can i use.com 

javascript가 사용가능한 브라우저들이 나옴.

### 다시 들어옴

package.json에 각종 데이터가 들어있음. dependency에는 각종 패키지가 

package-lock.json 는 자동적으로 만들어짐. 건드릴 필요는 없음.

npm이 사용하는 것, vue가 사용하는 것 자체의 의존성을 모두 깔아줌

node_modules에 그것들이 모두 들어가있음

gitignore로 처리되어 있음

각각의 개별 컴포넌트들을 정의해 나갈 것



### .vue 파일의 구조

<Template>
    
</template>

<script>
    
</script>

<style>
    
</style>

vscode에 ventur 깔기

components에 자식들의 정보를 넣는다.

ovenapp.io

간단한 mockup 할 수 있는 사이트

어도비 xd로 예쁘게 할 수 있음

sketch..(맥에서만 돌아감)



서버사이드는 모델부터 정의하고 템플릿이 나온다면 프론트는 템플릿을 우선하는 느낌이다.

vue 로 가장 위에 있는 단축키 이용하면 기본이 나옴

script에서 import를 해 두면 template에서 사용가능

"no-console" : "off"로 해두고 돌아온다.

자바스크립트는 장고랑 데이터가 흘러다니는 패턴이 틀려서 여러 가지 문제가 생길 수 있음. 

그래서 몇몇 데이터를 처리하는 관례들이 있음. 데이터는 APP에 만들어두고, 하위 컴포넌트에서 참조한다. 그것을 EMIT이라는 형태로 ...

일반적으로 구글 api 호출 (비디오리스트)

https://www.googleapis.com/youtube/v3/search?key=API_KEY&type=video&part=snippet&q=검색어

vue cli에서는 자동으로 env 파일을 관리해줌. 그것을 위해서 VUE_APP_ 으로 시작해야

파일명과 동일하게 파스칼케이스로 작성된 것을 template에서도 동일한 방식으로 사용한다. 기존 방식인 aaa-bb 같은 식으로 나오는 것과 동일

애로우 펑션 쓰지 말 곳 2가지만 기억 : addeventlistener, methods 안에서 함수 정의할 때



데이터를 자식이 부모에게 $emit(), 부모가 자식에게 props 

옵저버 패턴이 적용된 것.(공부해보셈)

props의 스텝은? 

1. 부모 컴포넌트에서 자식 컴포넌트의 template 태그에 v-bind를 통해 전달
2. 자식 컴포넌트의 props에 전달되어 있음





오늘 만드는 것

1. onInputChange 메소드 호출
2. youtube api 요청
3. youtube 응답받고
4. youtube response 비디오리스트 app component의 data로 저장
5. data가 업데이트되면 컴퓨넌트가 템플릿을 다시 렌더링함(vue가 해줌)
6. videolist 에서 변경된 결과를 보여줌



wappalyzer 등으로 체크해볼 수 있음 어떤 프레임워크를 사용하는지. 근데 100%는 아님.