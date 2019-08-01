max를 찾을 때도 약간의 차이를 줄 수 있다. 

그냥 `>`를 사용하게 되면 가장 앞에 있는 값을 찾을 수 있고 

`>=`를 사용하게 되면 가장 뒤에 있는 값을 찾을 수 있다



``` python
import sys
sys.stdin = open('input.txt','r')

```

입력 받아서 쓰는 방법





# 최빈값 구하기

```python
for t in range(int(input())):
    n,d=input(),input().split()
    print(f'#{n} {max(sorted(d)[::-1],key=d.count)}')
```

