fetch로 요청하고 응답을 받는다
fetch는 request object를 받아서 response object를 반환한다

fetch는 url말고도 응답을 받기위해 필요한것이 많다

const response = fetch('api.com')
이것을 실행하면 js는 보이지 않는 곳에서
const request = new Request('api.com', {
	method:'GET', // default value
}
	)

이렇게 필요한 정보를 넣어 request객체를 만들어서
const response = fetch(request) 이렇게 동작한다

fetch에 url만 전달하면 자동으로 url과 default 정보들을 넣어서 객체를 만들어 fetch로 전달한다

fetch는 비동기 함수다!, 데이터를 가져오는데 시간이 걸린다

fetch는 promise를 반환하며 그 promise객체는 나중에 성공적으로 데이터(response object)를 가져오거나 에러 데이터를 가져온다

대부분의 api는 데이터로 Json (파일을?) 리턴한다 그리고 이 데이터를 받기 위해 json함수를 이용해야 한다
json 함수도 비동기함수(promise를 반환한다) 이기 때문에 await으로 결과를 기다려야 한다

---

요청에 데이터를 함께 보내야 하는 경우
get요청일때는 url 파라미터(쿼리 문자열)에 필요한 정보를 함께 보낸다

정보를 숨겨서 보내야 하는 경우
어떤 api는 요청에 헤더를 필요로 한다

- 에러 핸들링 주의점
fetch는 일단 어떤 api에 접근에 성공했다면 에러가 발생해도 resolve로 에러 메세지를 전달한다, fetch함수 자체는 제대로 동작한것이다 (서버 에러)

api 서버에 '접근'하는데 실패했다면 그때에 reject를 실행한다, fetch함수의  요청 자체가 실패했다 (fetch 에러)


native는 뭔가 설치하지 않아도 되고 내장되어서 바로 사용할 수 있다는 뜻

fetch이전부터 썼던 데이터를 받아올수있는
XmlHttpRequest가 있다
