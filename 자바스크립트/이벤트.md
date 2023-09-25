#자바스크립트 #노마드코더 #jsEvent

document.querySelector를 이용해서 css선택자를 이용해서 요소에 접근할수있다

title = document.querySelector("h1");

그리고 js를 이용해서 css에도 접근할수있다

> 요소객체의 속성의 값도 객체일수있다!

title.style.color = "blue";

---

# event, addEventListener

js는 여러 이벤트를 listen하게 할수있고 
listen하다가 이벤트가 발생했을때 실행할 함수를 지정해 줄 수 있다

	1. js 에서 html 엘리먼트 찾기
	2. 엘리먼트에서 이벤트 리슨하기
	3. 이벤트에 반응하기(함수정의, 실행)

```javascript
const title = document.querySelector(".introduce h1");

let clickFlag = 1;

// 함수를 바로 실행하는게 아니기때문에 ()넣지 않는다.
// addEventListener(이벤트, 이벤트 발생했을때 실행할함수);
title.addEventListener("click", handleTitleClick);

function handleTitleClick(){
    if (clickFlag){
        title.style.color="blue";
        clickFlag=0;
    } else {
        title.style.color="grey";
        clickFlag=1;
    }
}

```


---

어떤 이벤트가 있는지 찾기
document의 속성을 확인해보면 on이 붙어있는 애들이 이벤트다

> on이 붙어있는 속성들!

window.addEventListener("copy", handleCopy);
이런식으로 window에도 eventListener 사용 가능하다
- 윈도우 이벤트 사용 가능
문서 참조하기

---

## js로 css 바꾸기

원래 js는 애니메이션, css는 스타일 담당이다
js로 html을 바꾸고 바뀐 html을 통해 다른 css를 적용할 수 있다

>  js -> html -> css


```javascript
const h1 = document.querySelector(".introduce h1");

function handleClick(){
    h1.classList.toggle("clicked");
}

function handleMouseEnter(){
    h1.innerText = "mouse enter!!";
}

function handleMouseLeave(){
    h1.innerText = "mouse out!!";
}

function handleCopy(){
    alert("copied something!!");
}

h1.addEventListener("click", handleClick);
h1.addEventListener("mouseenter", handleMouseEnter);
h1.addEventListener("mouseleave", handleMouseLeave);
window.addEventListener("copy", handleCopy);

```

title.className="new class name"; 
-> 엘리먼트의 클래스를 통째로 교체한다

## 엘리먼트객체의 classList의 함수 이용하기
title.classList.contains(clickedClass) 
document 요소객체의 classList객체의 contains, remove, add함수 이용한다

- contains
- add
- remove
- toggle // 토글함수로 제일 간단하게 구현 가능하다
