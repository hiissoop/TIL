```jsx
// 배열 전개
const arr = [ 1, 2, 3, 4, 5 ] 

console.log(arr) // [1, 2, 3, 4, 5] 
console.log(...arr) // 1, 2, 3, 4, 5

// 문자 전개
const str = "hello"

console.log(str) // "hello"
console.log(...str) // "h" "e" "l" "l" "o" 

// 객체 전개 
let obj = { name: "otter", gender: "male" } 

console.log(obj) // { name: , gender: }

// newObj 값을 변경하면, obj의 값도 같이 변경이 된다 
const newObj = obj

// newObj 값을 변경하면, obj의 값이 변경 되지 않게 한다
const copyObj = { ...obj } 

// but 아직까지 완벽한 복사는 아니다. (얕은 복사)

ex)

// 새로운 객체 생성
obj.hobby = { one: "shopping", two: "playing game"} ;

// 복사
let copyObj = { ...obj };

copyObj.hobby.two = "watching movie";

console.log(obj.hobby.two) // "watching movie" 
```