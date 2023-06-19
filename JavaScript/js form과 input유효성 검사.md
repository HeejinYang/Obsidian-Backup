#노마드코더 

```javascript
loginInput = document.querySelector("#login-form input");
loginInput.value.length
```

string 길이 확인하는법
stringName.length

---

## input 태그 유효성 검사하기

```html
<!-- form태그 안에 input이 있어야 브라우저가 직접 유효성 검사를 한다 -->
<form id="login-form">
        <input required maxlength="15" type="text", placeholder="What is your name?"/>
        
        <input type="submit" value="log in"></input>
       <!-- form태그 안에있는 버튼은 submit하는 기능을 한다-->
        <button>log in</button>   
</form>
```

- form태그 안에 input이 있어야 브라우저가 직접 유효성 검사를 한다
- form태그 안에있는 버튼은 submit하는 기능을 한다 / button의 type기본값이 "submit"이다.
-> 버튼의 type을 button으로 하면 제출이 안된다..
- submit하면 페이지가 재시작된다
-> 기본동작 실행 막기 event.preventDefault();

---

## 함수의 인자로 사용되는 event객체

이벤트의 기본정보를 받을수있게 함수의 인자로 뭔가 객체를 넣을수있다
그 객체는 아무 이름이나 상관 없는데 일반적으로 event라함

>이벤트로부터 얻을수있는 정보가 다양하다
>다양한 이벤트가 있다


form을 submit하면 브라우저는 기본적으로 페이지를 새로고침 하도록 되어있다. << 우리가 원하는 것이 아님!
event.preventDefault()로 기본동작이 실행되는걸 막는다

```javascript
const loginForm = document.querySelector("#login-form");
const loginInput = loginForm.querySelector("input");

function onLoginClick(event){
    event.preventDefault();
    console.log(loginInput.value);
    console.log(event);
}
loginForm.addEventListener("submit", onLoginClick);
```


---

## 새로운 방식의 문자열, 백틱 이용하기

```javascript
h1.innerText = `Welcome ${username}!!`;
```



