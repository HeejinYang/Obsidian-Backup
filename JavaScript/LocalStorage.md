#노마드코더 #자바스크립트

localStorage.setItem("username", "heejin");
localStorage.getItem("username");
localStorage.removeItem("username");

근데 localStorage자체가 object라서
localStorage.username="heejin";
이런식으로 해도 동작은 한다

## username이 존재하지 않는경우
localStorage.getItem("username"); -> null 반환
localStorage.username -> undefined 반환

const savedUserName = localStorage.getItem("username");
이런식으로 변수 이용할때 값만 복사되므로
localStorage에 username이 사라졌을때에도 값이 존재함에 주의하자