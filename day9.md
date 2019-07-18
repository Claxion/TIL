capitalize 함수는 맨 앞은 대문자로 나머지는 소문자로 바꾼다.



destructive method : 원본을 바꿈

nondestructive method  :  원본 변경 x => 할당해주는 것이 좋은 습관

return o : 

return x : 할당을 사용하면 안됨



.join 과 .split을 함께 자주씀

join은 str에 써야함.

<str구분자>.join(<list>)



제타위키 zetawiki.com

원본은 원래 immutable에 적용되는 개념..

<list>의 remove는 앞에서부터 삭제한다.

기본적으로 리스트는 뒤에서 들어가고, 뒤에서 빠져나옴(append, pop)

pop : destructive + return

pop 이 remove 보다 빠르다...

가능한 변수, 인수는 소문자로 시작하도록..



sort() , sorted() : sort는 원본 변경, sorted는 원본 변경 안함 

사용법 : sorted(lotto) , lotto.sort()

reverse(), reversed()



파이썬에서는 변수에 주소가 저장된다. 가리킨다.!!

숫자, 문자열, 참거짓 같은 경우에는 복사될 때 각각의 공간에 독립적으로 저장되지만

리스트는 복사될 때 주소만 복사되어 들어옴. : 대부분 mutable한 객체들의 경우 ! 

단순 대입시에는 numbers_copy = numbers 가 같은 공간을 가리키게 됨.



slicing operator도 좀 공부할게 있을듯

1차원 deep_copy 방법  : 
1) <list>[:]

2)  c = list(<list>)

2차원부터는 잘 통하지 않는다.

deep copy는 

```python
import copy
matrix3 = copy.deepcopy(matrix) 
```

튜플은 어차피 수정 불가능한 객체이므로 상관이 없다.



List Comprehension!!  (pythonic)

[<만들것> <반복문> <조건문>]

[ num+num  for num in numbers  if num %2 ==0]

예제를 가지고 공부좀 하자

if else가 있다면 조건식을 쓴다.

[f(x) if <조건식> else g(x) for a in as]



https://www.classcentral.com/course/coursera-an-introduction-to-interactive-programming-in-python-part-1-408



https://www.coursera.org/learn/interactive-python-1?



http://techneedle.com/archives/36833

http://pythontutor.com/live.html#mode=edit



http://composingprograms.com/



set comprehension도 가능
{word for word in words}

딕셔너리 pop()에 default 를 세팅해주면, 키가 없더라도 에러 내는 대신에 default 값을 돌려준다.

 dictionary.update()는 여러 개를 동시에 변경할 수 있다.



https://www.datacamp.com/community/tutorials/python-dictionary-comprehension#pdc



자료 : 만들고 읽고 수정하고 지우고 (CRUD)







