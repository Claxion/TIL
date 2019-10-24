monolithic architecture ( 서버 + 프론트를 하나의 구성으로 처리함)

서버와 프론트엔드서버를 분리함

SPA(싱글 페이지 어플리케이션) - 페이지 로드가 없음



MERN (mongoDB, express, react, node)



api 서버로 가자~ djangorestframework



더미데이터를 json으로 만들 수 있음



dumpdata 더미를 심자

 python manage.py loaddata musics/dummy.json

반대방향은  (뺄 때 넣을 때 )

python manage.py dumpdata musics > dummy.json --indent 2 

cat dummy



도메인/api버전/~~~



RESTful API

``` 

# music 
C          POST /musics
R(list)    GET  /musics
R(detail)  GET  /musics/:id
U          PUT  /musics/:id
D          DELETE /musics/:id

#comment restapi
C          POST /musics/:pk/comments
R(list)    GET  /musics/:pk/comments
R(detail)  GET  /musics/:pk/comments/:pk
U          PUT  /musics/:pk/comments/:pk
D          DELETE /musics/:pk/comments/:pk

```

Music:comment 1:n



이런 restful url이 너무 거지 같아서 facebook에서는 graphQL을 만들게 됨 

그럼 url이 없어지고, 보낼 정보들을 같이 보내서  db에서 처리하도록 함

(payload)



F12에서 XHR -> js가 우리를 대신해 자료를 보내준다. 요청을 분석해서 커스터마이징을 할 수도 있다.

postman 을 이용하여 테스트

