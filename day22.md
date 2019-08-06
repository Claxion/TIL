.col-3 으로 클래스가 있는 아이들을 쉽게 작성가능

justify-content-center

flexbox froggy를 가지고 연습

flexbox를 가지고 안에 있는 내용물을 컨트롤하게 됨. 외곽에서 내용물의 사이즈를 컨트롤하고 box 안에서 배치 방식을 컨트롤

x,y 축을 기준으로 항상 컨텐츠를 정렬한다.

flex direction 기본값은 row가 기본임.



배치의 어려움을 굉장히 많이 줄여주게 됨 

main 축을 기준으로 배치할 때는 justify-content /// flex-start, flex-end, center // space-between (컨텐츠 사이 균일 정렬), space-around(밖과 안쪽에도 균일 정렬)

display : flex 를 먹은 친구들이 flexbox가 됨

bootstrap의 row는 모두 flexbox였음

html은 쌓는 것은 되지만 각각의 여백을 주기가 어려웠음

메인 축에 대해서는 justify-content , 그 수직축에 대해서는 align-items



폭에 대해서는 컨텐츠 사이즈를 조절해 나감, 얌전히 쌓아나가기 위해서는 flex-wrap

여러행이 되었을 때는 자연적으로 너비, 높이 등이 조절이 됨(space-around)



animate.css

bootstrap 은 important 덕분에 더 세게 먹게 되어 있음

font awesome

codepen



반응형

meta=viewport (모바일이 생기면서 등장한 태그)

브라우저에서는 거의 화면 그대로의 크기임 

content는 딕셔너리처럼 동작함

width=device-width, initial-scale=1.0 (width 값에 대한 배율)  <- device  기기에 대한 정보가 들어감

@media (조건 ){ }

조건을 만족할 때 걸린 옵션



