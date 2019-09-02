BFS의 거리를 level로만 처리하지 않아도 괜찮다.

visited에 거리를 바로 저장해두는 방법이 가능. 



dx, dy를 튜플로 사용하자.

``` python
for dx, dy in [] :
    x  = x +dx 
    y = y+ dy
```



모든 정점간의 최단거리를 구하는 알고리즘. 

플로이드 워셜 알고리즘

```  python 
for k in range(V):
    for i in range(V):
        if i == k: continue
        for j in range(V):
            if j ==k or j == i : continue
            dist[i][j] = min(dist[i][j], dist[i][k] + dist[k][j])
            
if dist[start-1][end-1] == 1000:
    print("#%d" % tc , 0)
else:
    print("#%d" % tc , dist[start-1][end-1])
```



## 링크드 리스트

논리적 구조와 물리적 구조가 틀림