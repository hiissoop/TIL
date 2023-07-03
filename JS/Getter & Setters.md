Getter와 Setters는 캡슐화 하기 위해서 사용합니다.

사용자가 **잘못된 값을 이용할 수 없게 만드는 것**이 목표입니다.

```jsx
▾ get 구문은 객체의 속성 접근 시 호출할 함수를 바인딩합니다.

(바인딩하는 이유는 window나 다른 객체의 this를 불러오지 않기 위해서)

const obj = {
  log: ['a', 'b', 'c'],
  get latest() {
    return this.log[this.log.length - 1];
  }
};

console.log(obj.latest);       // log배열의 길이는 3 /  3 - 1 = 2가 나온다. 
                               // index값은 0부터 시작하기 때문에 0 = a, 1 = b, 2 = c

{get prop() { ... } }          // prop : 주어진 함수를 바인딩할 속성 이름
때로는 동적으로 계산한 값을 반환하는 속성이 필요하거나, 
명시적인 함수 호출 없이도 객체의 내부 변수 상태를 반영하는 값을 나타내고 싶은 경우가 있습니다.

어떤 속성에 접근자를 바인딩하는 동시에, 해당 속성이 값도 가지도록 할 수는 없습니다. 
그러나 접근자와 설정자(setter)를 함께 사용해서, 접근과 할당 모두 되는 '유사 속성'을 만들 수는 있습니다.

{get [expression]() { ... } }

▾ ex
다음 예제는 객체 obj에 유사 속성 latest를 생성합니다. latest는 배열 log의 마지막 요소를 반환합니다.

const obj = {
  log: ['example','test'],
  get latest() {
    if (this.log.length === 0) return undefined;
    return this.log[this.log.length - 1];            // length(2) - 1 = index[1];
  }
}
console.log(obj.latest);                      // "test"
```

- latest에 다른 값을 할당할 수 없다.
- 자세한 건 : https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Functions/get

```jsx
▾ set 구문은 객체의 속성에 할당을 시도할 때 호출할 함수를 바인딩합니다.

JavaScript의 설정자(setter)를 사용하면 지정한 속성 값의 변경을 시도할 때마다 함수를 호출할 수 있습니다.

▾ ex 다음 예제는 객체 language에 유사 속성 current를 생성합니다. current에 값을 할당하면, 해당 값을 log 속성에 저장합니다.
 
const language = {
  set current(name) {
    this.log.push(name);
  },
  log: []
};

language.current = 'EN';
console.log(language.log); 
// Expected output: Array ["EN"]

language.current = 'FA';
console.log(language.log);           
// Expected output: Array ["EN", "FA"]

▾ 계산된 속성 이름 사용하기

const expr = 'foo';

const obj = {
  baz: 'bar',
  set [expr](v) { this.baz = v; }
};

console.log(obj.baz);
//  "bar"

obj.foo = 'baz';
//  run the setter

console.log(obj.baz);
//  "baz"
```

- 자세한 건 : https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Functions/set