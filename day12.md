알고리즘 자체보다는 서비스할 때 에러처리를 할 일이 많이 생김.



왜 예외처리를 하는가? 사용자는 xxx이다. 어떤 것이 들어올지 모른다.

프로그램의 커버리지는 한계가 있고, 따라서 그 바깥부분을 예외처리로 하는 것이 좋다.



외부로부터 값이 들어올 때, 코드를 보내올 때는 가능한 한 처리를 하자.

여러 가지 예외를 같이 처리할 수 있다. 

우리의 디버그, 사용자가 확인이 필요할 때가 있으므로 구분이 필요~

```python
try:
    codeblock1
except (예외1,예외2):
    codeblock2
except 예외3:
    codeblock3
except:
    print('뭔가 에러남')
```

에러가 순차적으로 테스트되므로, 가장 작은 범주부터 확인할 것

예외 발생 여부에 상관없이 쓰려면 finally



저장하면 안되거나 하면 자료가 들어온다면 raise를 통해 에러발생

```python
raise

raise ValueError

raise ValueError('error')
```



bill gates steve jobs interview

pc guy mac puy



oop의 패러다임은 조금 더 사람이 이해하기 쉽게 철학적, 언어학적 개념으로 시작됨

반대로 절차적 프로그래밍은 순서도에 더 가까움

클래스에서 `__str__`는 print(class) 출력을

`__repr__` 는 그냥 출력을 바꿀 수 있다.



파이썬은 원래 객체로 구성되어서 동작이 특이한 부분이 있다.

처음에 각 클래스의 인스턴스를 생성하게 되면, 새로운 공간에 아무것도 없다. 인스턴스라는 것만이 지정되어 있음. 인스턴스의 어트리뷰트가 변경되면 그 때 변경된 데이터를 그 공간에 저장한다.

```python
class Person:
    name = 'unknown'
    lis = [1,2,3]
    def greeting(self):
        return f'my name is {self.name}'  
        
p1 = Person()
#p1.name = 'ww'
#p1.lis = [3,2,1] # 이 줄이 생략된 것과 아닌 것의 차이를 python tutor에서 확인해봐라
p1.greeting()
p1.lis.append(4)
```



상황에 따라서는 파이썬의 헷갈리는 클래스 구조가 전역적인 접근을 쉽게 해주는 부분도 있다. 

기본적으로 어트리뷰트에 리스트를 집어넣는 것은 잘 따져서 사용해야한다. 



# c# good good

#https://dotnetfiddle.net/