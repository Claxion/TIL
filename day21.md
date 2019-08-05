git credential reject

protocol=https

host=?!?!





css 사용할 때 꺽쇠 > 를 사용해서 트리구조를 따라 들어갈 수 있다. 

자식중에 누군가를 선택할 때 child~~ 사용	



n-th of type 

 같은 타입 중에서만 n 번째

n-of child 

 해당 요소의 하위요소들 중 n 번째 



div>p 스타일을 먹여놓으면 

div 바로 아래에 p가 있는 모든 구조에 다 적용하게 됨



div>span 으로 하게 되면 바로 아래에 있는 것만 찾아주는 자식 셀렉터

div span으로 하게 되면 어떤 위치든 아래에 있는 것을 찾아주는 후손 셀렉터



a+ ul : a 뒤에 오는 a의 형제인 ul를 찾음

a~ ul : a 뒤에 오는 모든 ul을 찾음



``` css
/* 속성 셀렉터 */
a[target="_blank"] {
  border : solid black 2px;
  border-radius: 5px;
  padding: 5px;
}

/* 값은 모르겠지만 class를 가진경우 */
/* inline-block일 경우에는 각자의 margin과 padding을 컨트롤하는 방법밖에 없다. */
ul[class] > li {
  width: 24%;
  height: 50px;
  display: inline-block

}
```



https://material.io/design/

materialize

cdn? content delivery (distribution ) network

css는 원래 가지고 있었던 것을 그대로 사용하는 경향이 있다.그래서 

reboot를 통해서 깔끔한 것에서 시작할 수 있도록 만든다.

bootstrap은 사용가능한 쉬운 미리 정의된 class들을 여러개 두고 있음

각종 클래스

mt ,pt , pb , mx

브라우저 기본 rem 은 16px 

가능하면 정사각형, 소형 모니터를 고려해서 container가 세팅되어 있음 와이드에서는 비어있음

그리드의 컬럼 사이의 폭은 padding으로 만들겠다.

모바일 기준은 한 row에 하나 보다 많은 컨텐츠가 들어가면 안됨

반응형이라는 것은 사이즈를 체크해서 그 순간에 되면 row를 풀어버리고 세로로 쌓아올림

sm 575 md 767 lg 992

