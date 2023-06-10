데이터 통신 ? [Promise]

```jsx
▾Promise {<pending>}
		‣[[Prototype]]: Promise
     [[PromiseState]]: "pending"
     [[PromiseResult]]: undefined

stack에 있는 console.log 
아직 callbackqueue에 있는 fetch함수 
데이터를 다 가져오지 못했으니, promise
```

- Promise의 3가지 상태
    1. fulfilled: 요청이 성공한 상태
    2. pending: 요청에 대한 응답을 기다리고 있는 상태
    3. rejected: 요청이 실패한 상태

```jsx
const promiseTest = () => {
		return new Promise((resolver, reject) => {
    // 응답에 성공 (fulfilled)
		resolver(100_응답);
		});
};
```

- setTimeout 설정

```jsx
const promiseTest = () => {
		return new Promise((resolver, reject) => {
		  // 응답을 기다리는 상태 (pending)
			setTimeout(() => {
					resolver(100_응답);
			}, 2000);
		});
};
```

- then으로 fulfilled가 될 때 까지 기다릴 수 있다. (pending상태에서 벗어남)

```jsx
const promiseTest = () => {
		return new Promise((resolver, reject) => {
		  // 응답을 기다리는 상태 (pending)
			setTimeout(() => {
					resolver(100_응답);
          // reject('error'): 요청이 제대로 이루어지지 않았을 때
			}, 2000);
		});
};

promiseTest().then((res) => {
		console.log(res); //fulfilled된 상태를 바로 보여줄 수 있다.
})
```

- fetch().then((res) ⇒ res.json())
- 받아온 데이터를 json형식으로 변환하는데에도 시간이 걸림  (pending)

```jsx
fetch()
.then((res) => {         // 서버 통신 기다리기
		return res.json();       
})
.then((res) => res {     // json 변환 기다리기
		console.log(json)
})
```

- JSON.parse()?: response headers가 존재하면 제대로 동작하지 않음
- catch()

```jsx
fetch()
.then((res) => {         // 서버 통신 기다리기
		return res.json();       
})
.then((res) => {         // json 변환 기다리기
		console.log(json)
})
.catch((err) => {
		console.error(err)   // 에러가 발생한다면 catch로 
})
```