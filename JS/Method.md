```jsx
// 화면에 element 추가하기

createElement();

// 숫자를 문자 타입으로 변환

toString();

// 입력값이 숫자가 아니면 true를 반환

isNaN();

// class가 있는지 체크, 추가, 제거, 토글

classList();
classList.contains          // 체크
classList.add
classList.remove
classList.toggle            // ⭐️ 있으면 가리고, 없으면 보이게 (코드 가독성 up)

// 동작 x

preventDefault();

// 브라우저에  key, value 저장

localStorage
localStorage.setItem(key, value);
localStorage.getItme(key);
localStorage.removeItem(key);

// 정수로 변환

parseInt();
// 소수점 버림

Math.floor();

// 공백 제거

trim();           // 앞 뒤 공백 제거

// 문자열 원하는 값만 변경

replace(찾는 값, 원하는 값)
replace(/찾는 값/gi, 원하는 값)  // 정규표현식

// 몇 초 뒤에 함수 실행 후 종료

seTimeout(함수, 시간)

// 일정 시간마다 함수 실행 

setInterval(함수, 시간)

//소수점 없애는 메서드

Math.round() // 반내림 반올림
Math.ceil()  // 올림
Math.floor() // 내림
```