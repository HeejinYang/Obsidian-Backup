array.forEach(sayHello);
배열의 각 요소를 sayHello의 인자에 넣어서 sayHello함수를 호출한다


array의 filter함수, forEach와 비슷하게 작동한다


array에서 뭔가를 지우면 사실은 array를 새로만드는것이다

filter에 인자로 들어가는 함수는 true 또는 false를 반환하고
true를 반환하는 인자만 배열에 남는다

그리고 fliter가 반환하는 배열은 새로 만들어진 다른 배열이다
