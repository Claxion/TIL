# python * 사용법

참조 : https://medium.com/understand-the-python/understanding-the-asterisk-of-python-8b9daaa4a558



## 1 multiple and power

``` python 
3 * 5 = 15 # multiple
2 ** 3 = 8 # power
```



## 2 repeatedly extending the list_type container

```python
zeros_list = [0] * 10   # output : [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
zeros_tuple = (0,) * 10 # output : (0, 0, 0, 0, 0, 0, 0, 0, 0, 0)
zeros_tuple2 = (0) * 10 # output : 0 (이 경우에는 int가 됨)

vector_list = [[1, 2, 3]] 
# output : [[1, 2, 3], [1, 2, 3]]
print(vector_list * 2)
for i, vector in enumerate(vector_list * 3):     
    print("{0} scalar product of vector: {1}".format((i + 1), [(i + 1) * e for e in vector]))
# output : 
#1 scalar product of vector: [1, 2, 3]
#2 scalar product of vector: [2, 4, 6]
#3 scalar product of vector: [3, 6, 9]
```

list와 튜플에 모두 적용된다. 만약 튜플에 사용할 때 comma를 생략하면 적용되지 않는다.

## 3 using the variadc arguments ! 

```python
def save_ranking(*args, **kwargs):
    print(args)     
    print(kwargs)
save_ranking('ming', 'alice', 'tom', fourth='wilson', fifth='roy') 
# output
# args => ('ming', 'alice', 'tom')
# kwargs => {'fourth': 'wilson', 'fifth': 'roy'}

```



`*args` means accepting the arbitrary numbers of *positional arguments* and `**kwargs` means accepting the arbitrary numbers of *keyword arguments*. In here, `*args`, `**kwargs` are called **unpacking**.

여러 개의 정해지지 않은 값들을 손쉽게 넣을 수 있음.  위의 경우에 포지션에 맞춰서 집어넣은 값(passed as positional)들은 tuple의 형태로 저장되고, key값에 근거해서 입력한 값(passed as keyword)들은 딕셔너리로 저장된다.

## 4 unpacking the containers

```python
from functools import reduce

primes = [2, 3, 5, 7, 11, 13]

def product(*numbers):
    p = reduce(lambda x, y: x * y, numbers)
    return p 

product(*primes)
# 이 때의 numbers : (2, 3, 5, 7, 11, 13)
# 30030

product(primes)
# 이 때의 numbers : ([2, 3, 5, 7, 11, 13], )
# [2, 3, 5, 7, 11, 13]
```

product 함수는 가변 변수를 받기 때문에 리스트 데이터 primes를 언팩해줘야한다. 이때 *primes 형태로 전달 가능. 이 때 primes는 언팩이 되었다가, 함수로 넘겨지면서 numbers라는 튜플로 저장된다.언팩하지 않은 상태로 전달하면 모든 요소가 아니라 리스트 자체가 들어간다.



# 5 just unpack the list or tuple

``` python
numbers = [1, 2, 3, 4, 5, 6]

# The left side of unpacking should be list or tuple.
*a, = numbers
# a = [1, 2, 3, 4, 5, 6]

*a, b = numbers
# a = [1, 2, 3, 4, 5]
# b = 6

a, *b, = numbers
# a = 1 
# b = [2, 3, 4, 5, 6]

a, *b, c = numbers
# a = 1
# b = [2, 3, 4, 5]
# c = 6
```

