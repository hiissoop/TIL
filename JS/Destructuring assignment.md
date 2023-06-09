- 구조화 되어 있는 배열, 객체와 같은 데이터를 destructuring시켜, 각각의 변수에 담는 것

```jsx
// 구조 분해 할당 전
const arr = [1, 2, 3, 4, 5];

const one = arr[0];
const two = arr[1];

// 구조 분해 할당
const arr = [1, 2];

const [ one, two ] = arr; (순회가 가능한 배열만) 

// 객체의 구조 분해 할당
const obj = { name: "otter", gender: "male" };

const { name, gender } = obj;

// 객체의 구조 분해 할당 변수는 새로 갊을 지정해줄 수 있다.

const { name: newName, gender: newGender } = obj; 
```