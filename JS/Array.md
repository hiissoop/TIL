### 배열 [🏠](https://www.notion.so/JS-8c7cc4b1a71448fb8c0fac3a66b33927?pvs=21)

- 배열에 있는 각 데이터의 위치: index

```jsx
const list = [1, 2, 3, 4];

idnex: 0 1 2 3 
length: 1 2 3 4
```

- const array = [”배열”]
- 초급
    - array.length: 배열의 길이 구하기
    - array[숫자(인덱스)]: 배열의 값 꺼내기
    - array.push(): 배열 맨 뒤에 값 추가
    - array.pop(): 배열 맨 마지막 값 삭제
    - array.sort(): 배열 요소 정렬
    - array.includes(값): 배열 데이터 확인

- 중급
    - array.concat(array2): 배열 2개를 연결
    - array.join(): 배열을 문자로 만들기
    - array.slice(): 배열 분리
    - array.filter(): 배열에서 원하는 요소 뽑기
    - array.map(): 배열의 모든 요소 변경

```jsx
const email = "codecamp@gmail.com"

email.includes("@")
true
email.split("@")
['codecamp', 'gmail.com']

const userMail = email.split("@")[0] = 'codecamp';
const userCompany = email.split("@")[0] = 'gmail.com';

const maskingMail = [];
maskingMail.pus(userMail[0]); x3 
askingMail.push("*"); x 4

maskingMail.join("") + "@" + company 
= code****@gmail.com
```