파이썬 스탠다드 라이브러리

pypi 파이피
다른사람이 만든 프로젝트, 모듈을 모아놓은곳

requests 모듈 사용하기
HTTP protocol

request가 정상인지 아닌지 확인하기
HTTP코드를 확인함


request 모듈을 이용해서 웹사이트를 가져올수있다?
request모듈의 get함수를 이용해서 웹사이트를 요청하고 응답을 받을 수있다

---
beautifulSoup이용해서 크롤링 해보기 #노마드코더

```python

# 웹사이트의 응답을 반환한다
response = get("웹사이트 주소")

if response.status_code !=200:
	print("response faild")
else:
	# "html.parser"는 html전달할거라고 알려주는것
	soup = BeautifulSoup(response.text, "html.parser")
	print(soup)

```

리스트의 요소 개수 알면 변수에 차례로 쉽게 대입 가능하다

```python
list_of_numbers = [1,2,3]
first, second, third = list_of_numbers

#first에 1, second에 2 이렇게 차례로 대입됨
```

