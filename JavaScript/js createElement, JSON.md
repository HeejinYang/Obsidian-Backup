#노마드코더 #자바스크립트 

태그이름 넣어서 엘리먼트 객체 만들기
const bgImage = document.createElement("img")
document.body.appendChild(bgImage);

여러줄 주석 
alt + shift + a
한줄 주석
ctrl + /


### 이벤트 리스너를통해 실행되는 함수의 event매개변수
event = 특정 이벤트
event.target = 특정 이벤트가 발생한 element
event.target.parentElement = 특정 이벤트가 발생한 element의 부모 element
event.target.parentElement.innerText = 특정 이벤트가 발생한 element의 부모 element의 innerText

이벤트 객체를 통해서 어떤 엘리먼트에서 이벤트가 일어났는지 확인할수있다

```javascript
// 버튼이 포함된 상위 엘리먼트 삭제하기
function deleteTodo(event){
    const li = event.target.parentElement;
    li.remove();
}
```

---

## JSON.stringify()
localStorage에 array 값들을 저장할수있고 텍스트 형식으로 저장된다 array자체를 저장할수없다
배열을 넣으면 값이 저장되긴 하지만 문자열로 저장된다
현재 배열의 상태를 저장한다, 값을 누적하는 방식이 아니다

```javascript
function saveTodo(){
    // JSON.stringify()를 이용해서 그냥 문자열이 아닌 배열 형태를 갖춰서 저장하게 한다
    localStorage.setItem("todos", JSON.stringify(todoArray));
}
```


## JOSN.parse()
문자열을 실제 객체로 변환함



