c++ 알고 기본 input output

dictionary key sort

```c++
#include<iostream>
using namespace std;

int main(int argc, char** argv)
{
	int test_case;
	int T;
	cin>>T;
	for(test_case = 1; test_case <= T; ++test_case)
	{
		char var1[10];
        char var2[10];
        cin>> var1 >> var2;
        cout << var1 << var2  << "\n";
	

	}
	return 0;
})
```



크롤러로 웹페이지 파싱할때 접하는 cp949 문제 '\xa0' 이놈!!!

[https://cnpnote.tistory.com/entry/PYTHON-%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EB%AC%B8%EC%9E%90%EC%97%B4%EC%97%90%EC%84%9C-xa0%EC%9D%84-%EC%A0%9C%EA%B1%B0-%ED%95%98%EC%8B%9C%EA%B2%A0%EC%8A%B5%EB%8B%88%EA%B9%8C](https://cnpnote.tistory.com/entry/PYTHON-파이썬-문자열에서-xa0을-제거-하시겠습니까)



``` html
clean_text = BeautifulSoup(raw_html, "lxml").get_text(strip=True)
print clean_text
# Dear Parent,This is a test message,kindly ignore it.Thanks


import unicodedata
text_string = BeautifulSoup(raw_html, "lxml").text
clean_text = unicodedata.normalize("NFKD",text_string)
print clean_text
# u'Dear Parent,This is a test message,kindly ignore it.Thanks'
```



```python
def Sort(sub_li): 
    sub_li.sort(key = lambda x: x[1]) 
    return sub_li 

sub_li =[['rishav', 10], ['akash', 5], ['ram', 20], ['gaurav', 15]] 
print(Sort(sub_li)) 
```