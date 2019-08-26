스택 밖에서의 우선순위와 스택 안에서의 우선 순위가 다른 경우 어떻게 처리할 것인가? 

스택 이용한 중위연산- >후위연산



스택에는 연산자만 들어감. top보다 우선순위가 높은 연산자인 경우 스택에 집어넣음



유망한 것에서만 진행.. 

뎁스 관리하는 것 하나의 변수만 둔다.



부분집합의 합 구하기

``` python
def backtrack(k, sum):
    global cnt 
    cnt += 1
    if k == N:
        if sum == 10:
            for i in range(1,11):
                if a[i]:
                    print(i, end=' ')
            print()
        else:
            k += 1
            if a[k] == 1:
                backtrack(k,sum+k)
            elif a[k] == 0:
                backtrack(k,sum)
 N = 10
a = [0] *(N+1)
cnt = 0
backtrack(0,0)
                
```

