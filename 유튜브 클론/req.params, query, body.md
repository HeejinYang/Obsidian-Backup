express의 req.params, req.query, req.body

1. req.params
라우터의 매개변수이다

router.get("/:id", home)

home 컨트롤러의 req.params.id로 url의 정보를 id변수를 통해 접근 가능하다
const id = req.params.id


2. req.query

템플릿에서 input에 get방식으로 정보를 전달하면 해당 input의 name 속성으로 값이 전달되고
이 값을 컨트롤러에서 req.query.name 으로 접근 가능

www.asdf.com?id=heejin&pw=1234


3. req.body

post방식으로 전달된 정보에 접근한다



