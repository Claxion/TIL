auth

authentication

- 회원가입
- 로그인

authorization

- 권한관리

model이 user라는 형태로 정리될 듯

일반적으로 id, email, password, password_confirmation.....



http는 원칙적으로 stateless 인데 로그인 정보를 지속적으로 유지하기 위해서는 state 처리가 필요함

cookie, session,  cache 등으로 처리함.



예전부터 로그인은 문제였음.

처음에는 로그인을 하게 되면, 그 흔적을 cookie로 사용자의 컴퓨터에 남겨두게 된다. 이게 다음 작업을 할 때 계속 서버로 전송되도록 해둔 것이 시초

쿠키의 탈취 가능성 때문에 로그인에는 사용하지 않는 방향으로 이동. 혹은 쿠키만으로는 사용하지 않음.

그러나 여전히 유용함. 비회원 장바구니 기능 등에서 사용할 수 있음



단순히 쿠키로는 사용하지 않고, 서버에 접속된 유저를 체크하는 방식으로 관리(ip .mac, cookie 등이 일치할 때만 ) -> 즉 정보를 관리하는 것은 서버에서 . 세션을 활용한다.



장고에서 

폼은 액션을 명시하지 않으면, 자기자신에게 돌아간다.!



usercreationform -> user에 대한 crud

authenticationform -> session에 대한 crud





템플릿에서 유저의 세션 정보 체크하는 것 user.is_authenticated

유저정보는 request.user에 들어있다. embed ->dir을 통해서 함수 확인가능

logout이 되어 있더라도 anonymoususer가 세팅되어 있음



데코레이터로 기본 로그인 세팅을 진행할 수 있다. 만약 기본 세팅과 다르다면 login_url을 인자로 전달해서 사용가능

@login_required(login_url='accounts/log_in')

혹은 

settings.py에 LOGIN_URL의 값을 바꿔주면 된다.



### ?? 

update 시에

post로 요청 들어옴 -> login_required -> 로그인 검증 -> redirect(next) (GET)