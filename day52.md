장고 pip install pillow

이미지 처리를 위해서



일반적으로는 추가 package를 깔고나면 installed apps에 넣어주자



장고 모델 메타 클래스를 집어넣어

ordering의 기본 옵션은 'pk'

메타는 orm을 건드리는 거라서 굳이 migration 할 필요가 없음



# 싱글 이미지 업로드

파일을 받아서 앱 안에 저장하고, 그 내부주소를 처리한다.



새로 모델 데이터를 추가할 때 기존에 존재하던 것들의 처리 문제가 발생.

파일을 넣기 위해서는 form에 enctype=multipart 

일반적으로 application이 기본값,  text/plain은 특수한 경우에만 사용한다.



파일 업로드

create페이지에서 파일을 올리면 class에 쭉 올라가서 views.py가 컨트롤 가능.

우리 루트 폴더에 파일을 저장해두고 image에는 파일명이 들어가있음

1. 저장되는 위치를 지정
2. 지정된 위치를 db에 넣어줘야

MEDIA_URL 지정

미디어 파일이 들어올 때의 주소도 알려줘야 함.

파일에 대한 url 요청은 static으로 



나중에 서버에는 AWS S3 storage에 파일 전용을 저장하고

나머지는 cpu나 이런 부분들을 이용한다



---

대표적인 static은 favicon 16*16 image

favicon generator 여러 사이즈의 favicon이 필요함



장고 transifex.com에 가서 번역 기여?



장고에 대한 static 파일의 기본 관례는 ?

app_name/static/app_name/image.jpg -> template 폴더랑 비슷하다

내 app 밑에 static 폴더를 만들자

쓰고 싶은 파일의 위치에 {% load static %} .

파이콘은 전부 공유하니까 mainapp 밑으로 옮겨준다 -> staticfiles_dirs 를 새로 정해줌

assets 라는 이름이 관례