```py
Matrix = [[0 for x in range(w)] for y in range(h)] 
```

2차원 배열 초기화 

box = [[0] * size for i in range(size)]

``` box2 = [[0]*size]*size  이건 안됨. 리스트 참조로 바뀌어버림

```

``` python
sumv = sum([tu[0]*tu[1]  for tu in zip(a,b)])
        #for ai in range(len(a)):
        #    sumv += a[ai]*b[ai]
```

파이썬에서는 함수 오버로딩을 지원하지 않음 ㅠㅠ . .

`__function__` 가 있는 메서드를 스페셜 메서드 혹은 매직 메서드라고 불림



class_method에는 클래스 관련된 것

static_method에는 클래스와 관련없는 연산들을 위주로 넣는다.

클래스 변수를 다룰 때는 가능한 클래스 메소드로 정의해서 사용하자

파이썬이 기본적으로 encapsulation을 지원하진 않는다. 다른 방법을 써야함..

객체의 연산자 오버로딩은 한쪽만 해주면 다른쪽은 알아서 처리해줌..



https://medium.mybridge.co/36-amazing-python-open-source-projects-v-2019-2fe058d79450



https://hackernoon.com/50-popular-python-open-source-projects-on-github-in-2018-c750f9bf56a0

여러줄 한번에 받기

```
for k in range(int(input())):    (n,m),a,b=map(lambda x: x.split(),(input(),input(),input()))    (n,m),a,b=map(int,(n,m)),list(map(int,a)),list(map(int,b))
```

