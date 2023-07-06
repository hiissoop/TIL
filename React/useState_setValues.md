```jsx
const handleChange = (e) => {
    const { name, value } = e.target;
    setValues((preValues) => ({
      ...preValues,
      [name]: value,
    }));
  };
```

여기서 setValue((preValues) => ({객체})

객체를 소괄호로 감싸는 이유는 문법을 짧게 쓰기 위함이다.

```jsx
setValues((preValues) => ({
      ...preValues,
      [name]: value,
    }));

이 코드를 풀어서 쓰면

setValues((preValues) => {
   return {
      ...preValues,
      [name]: value,
   };
});
```

화살표 함수에서, 소괄호 없이 바로 {} 중괄호를 쓰게 되면, 객체를 리턴하는 건지, 

함수를 실행하는 건지 알 수가 없어서 오류가 발생한다.

그래서 이걸 막기 위해 중괄호를 소괄호로 감싸주면, 
**함수 실행 부분이 아닌 객체를 리턴한다.** 라고 이해할 수 있다.

ex)

```jsx
(num) => num + 1 

여기서 num + 1 부분대신에 객체를 리턴하고 싶으면

(num) => { 어떤 값 } 이렇게 되어서 함수 실행 부분이랑 구분이 안됩니다.

그래서 이런 경우에는

(num) => ({ 어떤 값 }) 이렇게 해주어야 한다.
```