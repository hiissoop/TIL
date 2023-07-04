**▾ Class (template)**

```jsx

class person {
 name;             : 속성
 age;              : 속성
 speak()           : 행동(Method)
}

// 클래스는 껍질과 같다.
// 한 번만 선언한다.
// 데이터는 들어있지 않다.
// 메모리에 올라가 있지 않다.
// 껍질 안에 속을 채워주는 건 오브젝트
// prototype based
 class Person { 
 //constructor
 constructor(name, age) {
 //field
  this.name = name;                         //this는 객체를 가리킨다.
  this.age  = age;
 }
 //method 
 speak() {
  console.log(`${this.name} hello`);
 }
}

const dk = new Person('dk', 20);           //new를 붙임으로써 window에서 객체를 가리키게 되었다.     
console.log(dk.name);
console.log(dk.age);
dk.speak();   
```

**▾ Getter & Setters**

```jsx

class User {
 constructor(firstName, lastName, age) {
 this.firstName = firstName;
 this.lastName = lastName;
 this.age = age;
 }
}

const user1 = new User('Steve', 'Job', -1)
console.log (user1.age)    :   -1          // 나이가 -1인 것은 이상하다.

그렇기 때문에 Getter, Setters를 사용해주며 사용자의 입력을 방어한다.

get age() {           // 값을 리턴
 return this._age 
}

set age(value) {      // 값을 설정 
 this._age = value;   // 여기서 _age를 age로 하게 되면 Call Stack이 가득 차게 된다.
                      // function hello() {
                      //   hello();
                      // }    자기 자신을 계속 부르는 것과 같다.                  
}

set age(value) {    
 if(value < 0) {
   throw Error ('age can not be negative');      // 이렇게 경고를 보낼 수 있다.
 }
}

 &

set age(value) {
 this._age = value < 0 ? 0 : value;             // 이렇게 마이너스 값이 들어오면 조용히 0으로 값을 변경할 수 있다. 
}
```

**▾ Public, Private**

```jsx

class Experiment {
 publicField = 2;
 #privateField = 0;
}

const experiment = new Experiment();
console.log(experiment.publicField);       // 2
console.log(experiment.privateField);      // undefined 
```

**▾ Static**

```jsx

class Article {
  /*static*/ publisher = "DK";
  constructor(articleNumber) {
    this.articleNumber = articleNumber;
  }
  /*static*/ printPublisher() {
    console.log(Article.publisher);
  }
}
const article1 = new Article(1);
const article2 = new Article(2);
console.log(article1.publisher);        :  "DK"    / static을 붙이지 않으면 아티클을 계속 불러내어야 한다.

static = console.log(Article.pulisher)  :  "DK"    / static은 클래스 자체에 붙여준다.
```

**▾ Inheritance / extend**

```jsx
▾ Inheritance / extend

class Shape {
  constructor(width, height, color) {
    this.width = width;
    this.height = height;
    this.color = color;
  }
  draw() {
    console.log(`drawing ${this.color} color of`);
  }
  getArea() {
    return this.width * this.height;
  }
}

class Rectangle extends Shape {}
class Triangle extends Shape { // 필요한 함수만 오버라이딩 할 수 있다. (상속의 장점)
  draw() {
    console.log("▾");         // 새로 정의한 함수만 호출되는 걸 알 수 있다.
    super.draw();             // 만약 부모의 함수도 부르고 싶다면? 'super'를 붙여주자.
  }
  getArea() {
    return (this.width * this.height) / 2;
  }
}

const rectangle = new Rectangle(20, 20, "blue");
const triangle = new Triangle(20, 20, "red");

console.log(rectangle.getArea()); // : 400
console.log(triangle.getArea());  // : 200
triangle.draw(); // : ▾, drawing red color of

```

**▾ InstanceOf**

```jsx

console. log (rectangle instanceof Rectangle);      // true;
console. log (triangle instanceof Rectangle);       // false;
console. log (triangle instanceof Triangle);        // true
console. log (triangle instanceof Shape);           // true
console. log (triangle instanceof Object);          // true  자바스크립트의 class는 object에 상속 되어 있다.
 * https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects
```