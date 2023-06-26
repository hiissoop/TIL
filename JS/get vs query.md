getElement는 query에 비해 1.2~.1.3 빠르다.

query는 getElement에 비해 생산성이 훨씬 높다.

id, class, [data-*=""],input[name=""]등 다양한 선택자를 사용할 수 있다.

```jsx
<form id="userForm">
  <input id="username" type="text"/>
</form>

// getElemenyById를 이용했을 때
const username = document.getElementById("username");

// querySelector를 이용했을 때
const username = document.querySelector("#userForm #username");
```

▾ HTMLCollection

- getElementsByClassName의 반환값
- 유사 배열
- 인덱스나 반복문을 통해 요소에 접근 가능하나 배열 메서드는 사용 불가
- Live Collection
- DOM 변경 사항이 실시간으로 반영됨

▾ Node List

- querySelectorAll의 반환 값
- 유사 배열
- 인덱스나 반복문을 통해 요소에 접근 가능하나 배열 메서드 사용 불가
- forEach(), entries(), keys(), values()는 사용 가능
- Static Collection (Non-Live Collection)
- DOM의 변경 사항이 실시간으로 반영되지 않음
- (대부분 NodeList는 Live Collection지만 querySelectorAll의 반환 값은 Static Collection입니다.)