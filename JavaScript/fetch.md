fetch로 요청하고 응답을 받는다
fetch는 request object를 받아서 response object를 반환한다

fetch는 url말고도 응답을 받기위해 필요한것이 많다

const response = fetch('api.com')
이것을 실행하면 js는 보이지 않는 곳에서
const request = new Request('api.com', {
	method:'GET',
}
	)

이렇게 필요한 정보를 넣어 request객체를 만들어서
const response = fetch(request) 이렇게 동작한다

fetch에 url만 전달하면 자동으로 url과 default 정보들을 넣어서 객체를 만들어 fetch로 전달한다

fetch는 비동기 함수다!
fetch는 promise를 반환하며 그 promise객체는 나중에 성공적으로 데이터를 가져오거나 에러 데이터를 가져온다

fetch가 가져오는 데이터의 정체

요청과 함께 파라미터에 인자 보내는 방법
get요청일때는 쿼리 문자열에 필요한 정보를 함께 보낸다


