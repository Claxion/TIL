협업도구



깃!!



1. 코드 관리

-  scm 소스 코드 매니지, vcs 버전 컨트롤

2. 원격저장소

- github, gitlab, bitbucket

3. 협업 도구

- push & pull, fork & pr, branch & pr

4. 이력서





GET, post 이외의 다른 전달 방식이 많다.

그래서 post를 기준으로 나머지를 처리하자.



슬랙과 홈페이지를 연결하기 혹은 텔레그램과 연결하기

-> 어떤 사람이 보낸 메시지를 인식하고 그거를 체크해서 돌려준다.

-> getUpdates를 계속하는 방식으로 가능 

-> 그것을 좋게 해결해주는 방식이 webhook 

-> telegram을 통해서 보내는 신호/정보를 webhook에 받는다.

-> 요청을 받을 곳이 어딘지를 알려줘야 한다. 



ngrok 다운받은다음

cmd에서 ngrok.exe을 실행하고 

ngrok http 8000 같이 포트를 설정해준다.



중간에 csrf 문제

```
from django.views.decorators.csrf import csrf_exempt@csrf_exempt
```



1. wehook을 설정한다 (setwebhoo
2. webhook 정보조회 getwebhookinfo
3. 정보정리. deleteWebhook 및 재설정
4. settings.py 에 allowed_hosts 에 ngrok 주소를 넣어준다.
5. 장고의 경우 관례때문에 setwebhook 단계에서 마지막에 slash를 꼭 넣어줄 것
6.  json으로 돌려줌.

res = json.loads(request.body)



슬랙 webhook, telegram webhook 

