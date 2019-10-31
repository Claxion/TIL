sync , async 

non-blocking

hoisting

몇몇 자바스크립트의 함수는 비동기적으로 non-blocking 하게 구현되어 있다. 

브라우저의 조작을 위한거기 때문에, 브라우저가 정지되면 안됨.



async 

- what
- why
- now 
  - callback
  - asynchoist
  - promise (주로 사용할 예정)



비동기적으로 동작하는 함수 (입출력에 관련된 것들이 많음)

settimeout,  fileread, filewrite



비동기함수는 바로 받을 수 없다. 병렬적이므로, 받았을 경우에 undefined가 나옴

일단 끝난 다음에 콜백으로 되돌려줄 것을 결정함.



일반적인 웹요청 axios 사용



장고 백엔드 위에 자바스크립트로 좋아요 기능 구현.

이벤트리스너에 넣을 때는 애로우 펑션 => 을 사용할 수 없다.