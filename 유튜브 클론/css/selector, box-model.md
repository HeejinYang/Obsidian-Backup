- 선택자로 한 페이지 내의 요소 선택하기

```
.classname{

}

#idname{
속성:값;
속성:값;
}

p.classname{ // 태그와 클래스 함께 선택

}

p, div, h1{ //여러 선택자 동시에 스타일 적용

}

*{
}
```

- css연결
외부파일 <link rel="stylesheet" href="style.css"> 
html내의 style태그에 작성하기
태그 자체에 작성하기 - 인라인 태그

- box-model
element의 margin, border, padding, content

margin, padding-
top, right, bottom, left

border width, style(required), color

패딩, 마진은 transparent하다!


- margin collapse
엘리먼트 간에 마진의 top, bottom이 겹칠때는 큰 마진으로 합쳐진다
right, left말고 top, bottom에만 적용됨

색깔 속성값
rgb(0,0,0)
\#ffffff
predefined ex) tomato, aqua, cadetblue...

---

width
height
-> 컨텐츠의 영역을 설정한다! 마진, 보더, 패딩을 제외한 content

%는 부모의 컨텐츠 내에서 자신의 마진, 보더, 패딩을 뺀 컨텐츠가 차지할 수 있는 영역내에서 해당 %를 차지한다
margin:auto는 가능한 영역에서 자동으로 가로에서 center가 된다
중요한거는 부모 엘리먼트 내에서 가능한 영역을 나눠갖는다는 것
%도 마찬가지

max-width는 화면이 클때에는 max사이즈로 보여주고 화면이 작아지면 스크롤바없이
자동으로 반응형으로 차지하는 영역이 작아진다

width만 설정하면 화면이 작아졌을때 스크롤바가 생긴다


box-sizing: border-box;
width가 설정되어 있고 padding도 설정되어 있을때 width속성값에 맞춰서 사이즈가 조절된다




