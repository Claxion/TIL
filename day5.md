# Telegram bot 만들기

1) Telegram 설치 

2) @botfather 검색 

3) botfather 채널 인

4) /new bot : 새 봇 만들기

5) 봇의 이름 : jinjin

6) 봇의 username : jinjin1_bot

7) bot token 생성



// https://core.telegram.org/bots/api 메뉴얼

주소를 interpolation 을 이용해서 사용한다.

내부 로직을 수정할 경우에는 서버를 껐다 키자. 수정이 잘 되는 건 html 정도임.

텔레그램에 글자, 파일, 그림이 모두 다른 키값을 가지고 있음.

그리고 텔레그램의 파일 혹은 사진은 서버에 접속해서 다운받아올 수 있음 

* json 을 쉽게 보기위해 pprint 패키지 사용



# 키값은 숨겨두자! 

환경변수로 바꿔서 넣어두자.

 echo $PATH 로 갈 수 있다. 

윈도우, 리눅스, 맥 모두 다름.

 python decouple : 변수의 설정 자체를 분리하자

전역변수는 대문자로 쓰는 것이 관례 

.env 파일로 보관

.gitignore 파일을 만들자.

.git 파일을 여러 개 상-하위 폴더로 구축하는 것은 최대한 피하자



# User가 메세지를 보내면 상태변화를 인지할 수 있다.

setWebhook!! Telegram아 메세지가 오면 우리에게 메세지를 보내줘~

일반적인 test 라인은 local 환경에서 구축되기 때문에 메세지를 받을 수가 없다. 

이 때 필요한 것이 ngrok

일반 user 위치에 저장

ngrok http 5000 (외부포트번호)

https://e2e70a24.ngrok.io -> http://localhost:5000 (외부에서 저 주소로 접속가능)

https://apl.telegram.org/bot{token}/setWebhook?url={내 외부주소}/{token}

앞으로 보내지말라고 하려면 deleteWebhook





## 사용한 api

 getUpdates , getMe  , sendMessage , setwebhook, 

webhook을 세팅하면 getupdate는 사용할 수 없다. (수동적인 업데이트를 주기적으로 받기 때문에 self update는 불가능)



# naver developer

request에 대한 이해가 필요함.

