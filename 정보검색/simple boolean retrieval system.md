컴퓨터가 처음부터 스캔해서 찾는 방법 = Grepping through text

## Simple Boolean retrieval system

### term document incidence matrix
단어 term, 문서 document (t,d) 행렬

단어가 나온 문서는 1, 아니면 0이 채워진 행렬
벡터를 비트연산하면 원하는 정보를 얻을 수 있다

문서의 양과 크기가 커지면 용량이 어마어마하게 커진다
->대신에 inverted index를 만들자


### inverted index
단어를 추출함
단어에 단어가 나온 문서 번호들을 표시한다
dictionary, postings file


forward index = 문서번호에 내용을 매핑
inverted index = 내용에 문서번호를 매핑


- 단어가 둘다 나오는 문서 찾기 알고리즘
intersecting two postings lists
문서번호를 비교해서 같으면 해당번호 기록하고 현재 보고있는 문서번호 다음으로 번호로 증가
다르면 둘 중 작은쪽 문서번호를 다음번호로 증가시킨다(다음 문서를 가리킨다)

시간복잡도는 선형함수다 n (order of n?)
posting의 개수만큼 연산함

> posting이 sorting되어 있을때 가능하다!

---

불리안 리트리벌 모델

and, or, not 으로 쿼리를 만드는것 = 불리안 쿼리

문서를 단어의 집합으로 본다

단어간의 의미가 사라져 정확성이 떨어지지만 빠르게 정보를 얻을 수 있다

30년간 이용된 검색도구였다

---

westlaw
미국에서 쓰이는 법률정보검색 시스템

상업비밀노출을 방지하기 위한 법적인 이론 검색하기

near
/s 문장내에서 찾아라
/3 세 단어 내에서 찾아라
/p 문단 내에서 찾아라
쿼리를 세밀하게 해서 현재도 불리안 쿼리를 사용하고 있다


---
쿼리 최적화
쿼리를 처리하는 순서를 바꿔주는것
개수가 적은 term에대한 연산 먼저 하기

term을 increasing frequency order로 정렬한다




