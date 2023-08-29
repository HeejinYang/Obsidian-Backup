## first class function
어떤 언어에서 함수가 변수처럼 다뤄질 수 있으면 그 언어는 일급함수를 갖는다고 한다

1. 변수처럼 함수를 변수에 대입 가능
2. 함수를 반환 가능
3. 함수를 인자로 전달 가능

---

## Callback

콜백함수는 일급함수를 쓰는 자바스크립트에서 함수의 인자로 전달되어 함수 내부에서 호출되는 함수다

비동기 함수 내에서 (콜백)함수를 호출하여 어떤 일이 순차적으로 진행될 수 있게 한다
비동기 함수의 제일 마지막에 콜백함수를 호출하여 다음 할 일을 실행한다
(비동기 함수가 처리된 후에만 해야하는 일이 있는데 그일을 비동기함수 내에서 콜백함수가 실행하도록해서 순서대로 실행되도록 하였다)

비동기함수 = 응답이 언제 올지 모르는 함수, 일이 언제 끝날지 모르는 함수, js는 응답을 기다리지 않고 다른 일을 수행한다

<콜백으로 비동기 함수를 처리할때의 문제>
1. 가독성이 떨어진다 (콜백 지옥)
2. 코드의 논리를 알기 힘들다
3. 하나의 함수가 여러가지 일을 한다

이를 해결하기 위해 Promise 객체를 이용한다

---


## Promise

promise(약속)을 하는 사람, 받는 사람이 있듯이
promise객체를 만드는함수, 객체를 받아서 사용하는 함수가 있다

promise객체를 이용해서 아직 얻지 못한 (미래에 얻을) 데이터를 가지고 할 일을 작성한다

promise객체는 기차 티켓 같은 것

- promise객체의 세가지 상태
pending
promise내의 resolve를 호출하면 resolved or fulfilled
promise내의 reject를 호출하면 rejected상태

```javascript
function getWeather() {
  return new Promise(function (resolve, reject) {
    resolve('sunny'); // 다음 호출하는 함수의 인자로 넘어간다
    // reject('network error');
  });
}

function func2(weather) {
  return new Promise(function (resolve, reject) {
    resolve(weather); // sunny
    // reject('network error');
  });
}

function onSuccess(data) {
  console.log(`success: ${data}`);
}

function onError(error) {
  console.log(`Error: ${error}`);
}

getWeather()
	.then(func2)
	.catch(onError); // 전역적으로 에러가 일어나면 실행된다

// then에 두번째 인자로 에러핸들러 함수를 넣을 수도 있고 catch로 전역적으로 에러를 다룰수도 있다
// then으로 에러를 다루면 그 다음 then이 계속 실행된다
```

promise객체의 then, catch, finally 함수
catch는 전역적으로 에러를 다룸