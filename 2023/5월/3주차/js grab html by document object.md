#자바스크립트 #document #getElement

## document object

html이 js와 css를 가져오고 브라우저에서 html을 통해서 둘이 실행된다 
반대로 js는 js의 document객체를 통해서 html에 접근, 수정이 가능하다

document객체에 웹사이트의 html 들어있다

```javascript
// html코드를 보여줌, 그냥 출력
console.log(document);

// 객체의 정보를 속성, 값 형태로 보여줌
console.dir(document);

// document객체를 이용해서 html내용 수정하기
document.title="web site new title";
```


js가 적용된 결과를 브라우저에서 보여준다

---

## js로 html element 가져오기

document객체에 '이미 정의된 함수'와 태그의 id, or class 를 이용해서 html태그의 내용을 가져올수있다

요소 하나에도 속성이 어마어마하게 많다!
```javascript
title = document.getElementById("h1id");

console.dir(title);
// 요소 하나를 객체로 가져온다, 요소 하나이지만 그안에 속성이 되게 많다!!

console.log(title);
//하나의 태그를 코드로 출력한다
```


- getElementById("id") : 요소 한개 객체로 반환
- getElementsByClassName() : 배열로 순서대로 반환, 각각은 객체임
- getElementsByTagName() : 태그이름 순서대로 배열로 반환
- document.querySelector(".classname \#id div")   /css 처럼 순서대로 가져오기?
- document.querySelectorAll

heejin[0].innerText = "new text";
이런식으로 배열로 각 요소에 접근 가능하다

getElementsByTagName("p") 이것도 요소를 배열로 가져온다

---

## getElementBy 대신에 querySelector 사용하기
### (feat.css selector)


제일 좋은 방법 querySelector
css처럼 사용할수있다
중복된게 있으면 제일 위에있는거 하나만 선택한다!!!!

querySelectorAll 은 배열로 모두 가져옴

