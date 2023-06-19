#자바스크립트 #노마드코더 #NaN

사용자로부터 값을 입력받기

옛날버전 
prompt함수 이용한다 , 반환: string
반환한것을 int로 바꿔주기 -> parseInt()이용한다

```javascript

// age에 문자 입력하면 NaN이 age값으로 들어간다
// 그런데 parseInt한 결과의 typeof 는 number가 나온다..
// 값은 NaN이지만 type은 number?
const age = parseInt(prompt("how old are you?"));
console.log(age);


```

NaN = Not a Number  '숫자로서 정상정인 값이 아니다'
값자체는 NaN이고 type이랑은 약간 다른 개념인것같다.?

ㄴㄴ 걍 숫자는 맞는데 계산이 안된다는뜻(인것같다)

조건문 다른 언어랑 같음

---

## \=\=\= 연산자

!\=\=연산

논리연산자 and, or && ||


\=\=연산은 값만 비교한다
ex) 0\=\=false -> true
\=\=\=연산은 값과 자료형도 비교한다
ex) 0\=\=\=false -> false

=== 을 사용하자

> 자바스크립트는 사용자와 상호작용하기 위해 만들어졌다!!





