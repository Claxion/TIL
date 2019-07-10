# flask

## 기초

- pip install flask
- @app.route("/주소") 형태로 사용 -> 그 밑에 함수 def 및 인수처리가 가능

* return 값에는 str만 허용된다. 
* return 값에 ""가 들어오면 에러가 발생(따로 처리가 필요)
* 파일이 있는 git 위치에서 실행해야 정상 실행됨 (local 기준)

- 실행시에는 flask run 이후 재실행

- print 로는 우리 command로 날라오고, return 은 브라우저로 날라감

- 자동재시작을 하는 경우에는 python - (filename).py로 실행함

  ```python
  if __name__ == '__main__' :
  	app.run(debug = True)
  ```

  



## flask html 리턴

``` python
from flask import Flask, render_template
import random

app = Flask(__name__)
## __name__ : execution context? 

@app.route("/")
def home() : 
    #return render_template("넘겨주는 템플릿 파일이름")
    return render_template("home.html")

@app.route("/hello/<name>")
def hello(name) : 
    #name에는 hello 이름 활용가능.
    # <name> == empty string 인 경우는 도저히 해결이 불가능한가? 
    if name != None :
        return render_template("hello.html", usename=name)
    else : 
        return render_template("hello.html")
```

stack overflow 에 질문 ~~



## 기타

```python
from flask import Flask
```

html : hypertext markup language 각종 역할을 마킹.

mark down ? : markup의 불편함 때문에 나옴. 역할은 비슷함.

최초의 홈페이지  cern , tim burners lee

** live server ** (vscode extension install) : open with live server 자동갱신

html + css 형태로 발전

python random.choice 는 dictionary 에 바로 사용할 수 없음. 리스트에 적용해야 함.



# html vs markdown

# 제목 : <h1></h1>

## 이건 중제목 : <h2></h2>

### 소제목 : <h3></h3>

본문 : <p></p>

하이퍼링크 : <a href=""></a> (anker?, hyper reference - need to input exact refer) 

만약 http를 입력하지 않으면, 로컬에서 해당 페이지를 검색해서 움직인다.

그림 : <img src="" > 

동영상 : <iframe src = "">

리스트 :  <ul> <ol> <li>

ol은 잘 사용하지 않음

vscode 에서 ! + tab 사용하면 기초 아웃라인을 잡아줌.



## json viewer chrome extension 

github.com/sspy21



