▾ this는 무엇인가?

- this는 함수를 호출하는 방법에 따라서 가리키는 값이 달라진다.

```jsx
let obj = {
  a: function () {
    console.log(this);
  }
}
obj.a(); //obj     this는 객체를 가리키고 있다

let b = obj.a;
b();    //window  this는 obj.a를 객체에서 꺼내온 것이기에 window를 가리키고 있다.
```

▾ bind는 무엇인가?

- es5에서 this의 호출하는 방식에 개의치 않는 bind(메소드)를 만들었다.

```jsx
var obj2 = { 
    c: "d" 
};

function b() {
  console.log(this);
}

b();                 // Window
b.bind(obj2).call(); // obj2
b.call(obj2);        // obj2
b.apply(obj2);       // obj2

//위의 세 개 메소드를 쓰게 되면 this가 객체로 바인딩 된다.
• 선언한 function의 this는 항상 window (strict 모드에서는 undefined )
```