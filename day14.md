dictionary key sort

    x = {1: 2, 3: 4, 4: 3, 2: 1, 0: 0}
    sorted_x = sorted(x.items(), key=lambda kv: kv[1])

python matrix transpose

```py
list(map(list, zip(*l)))
```

2*2 => 1 flatten

```python
flat_list = [item for sublist in l for item in sublist]
```









깃 협업

repo master

README.md 한 사람이 만들고 



`ls.git` git의 head

`cat .git/config`

git hub - issue에 발행가능

@ 을 통해서 멤버 호출가능 : 기본적으로는 메일로 푸시옴

## 협업 시나리오

가장 쉬운 것 : 시간을 분리하거나, 파일을 분리하거나해서 사용한다 => 팀 리더가 일을 분배해야함



git flow, github flow , git lab flow

merge할 때는 merge conflict라고 표시해주자

되도록이면 동일파일/동시간에 건드리지 않는다.





### local

| status | staging area | commit log |
| ------ | ------------ | ---------- |
|        |              |            |
|        |              |            |
|        |              |            |

필요한 파일만 명확하게! 선택적으로 적용할 수 있다.

git add . 'commit.py'



`git reset --hard <commt>`

`git check out master[branch name]`

사진을 찍는 개념



commit을 한 것을 하나의 커밋에 추가하고 싶을 때 rebase를 이용한다.



## 버전명

semantic versioning : 3.3.3 major, minor, patch

주로 patch는 버그픽스, minor는 기능적 추가일 가능성이 높음. major 가 바뀌면 문법도 바뀌어서 안될수도 있음





### flask 추가

routing은 kwargs로 정의되어 있음

