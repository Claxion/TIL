# 전기버스 문제풀이

충전소를 미리 배열로 체크해놓음 충전소가 있는 자리는 배열에 1을 넣어둔다

pre는 버스의 이전 위치, cur는 현재 위치

```python
T = int(input())
for tc in range(1,T+1):
    K, N,M = map(int, input.split())
    charging_stations = list(map,int,input().split())
    stations= [0]*(N+1)
    for i in range(M):
        stations[charging_stations[i]] = 1
        ~~
    cnt = cur = 0
    while True:
        pre = cur
        cur += K
        if cur >= N:
            break
        if stations[cur] == 1:
            cnt +=1
        else:
            for i in range(1,K+1):
                if stations[cur-i] == 1:
                    cur -=1
                    cnt +=1
                    break
            if cur ==pre:
                cnt = 0 
                break
print("#%d %d" % tc, cnt)
```



프로의 중요한 덕목 : 

Do not recompute



전치를 활용해야할듯..

부분집합을 만들 때 bit 를 생각해보자.

어떤 값에 비트로 두번 xor를 하게 되면 자기자신이 나옴 

비트를 이용해서 부분집합을 생성할 수 있다 .

적절한 타이밍에 중단하는 것도 중요한 덕목



이진검색, 보간검색의 퍼포먼스는 같다.