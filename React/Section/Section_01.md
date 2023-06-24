### `Nodejs, npm, yarn 이해`

- CLI

| 명령어 | 기능 |
| --- | --- |
| pwd | print working directory. 현재 작업 중인 폴더 정보를 출력합니다 |
| cd | change directory(폴더). 경로를 이동합니다. 절대 경로, 상대 경로로 이동이 가능합니다. |
| ls | list. 현재 폴더 안에 있는 목록을 확인합니다. |
| cp | copy. 파일 혹은 폴더를 복사합니다. 폴더를 복사할 경우에는 -r 옵션을 함께 사용해주어야 폴더 안에 있는 목록도 함께 복사할 수 있습니다. |
| mv | move. 파일 혹은 폴더를 이동합니다. 실제로 원하는 위치로 이동할 때도 사용하지만, 이름을 변경할 때도 사용합니다. |
| mkdir | make directory. 폴더를 생성합니다. -p 옵션을 주면 하위 폴더까지 한 번에 생성 가능합니다. |
| rm | remove. 파일이나 폴더를 삭제합니다. 폴더를 삭제할 때는 -r 옵션을 주어야하며, -f 옵션을 주면 사용자에게 삭제 여부를 묻지 않고 강제로 삭제하게 됩니다. 폴더를 삭제할 때에는 하위 폴더까지 모두 삭제되므로 유의합니다. |
| touch | 파일이나 폴더의 최근 업데이트 일자를 현재 시간으로 변경합니다. 파일이나 폴더가 존재하지 않으면 빈 파일 혹은 폴더를 생성합니다 |
| cat | concatenate. 파일의 내용을 출력할 수도 있고, 파일 여러 개를 합쳐서 하나의 파일로 만들 수도 있습니다. 또는 기존 한 파일의 내용을 다른 파일에 덧붙일 수도 있습니다. 새로운 파일을 만들 때에도 사용됩니다. |
| head | 파일의 앞 부분을 보고싶은 줄 수만큼 보여줍니다. 옵션을 지정하지않으면 상위 10줄을 보여줍니다. |
| tail | 파일의 뒷 부분을 보고싶은 줄 수만큼 보여줍니다. 옵션을 지정하지않으면 하위 10줄을 보여줍니다. -f 옵션과 함께 실행하면 파일 내용을 화면에 계속 띄워주고 파일이 변하게되면 업데이트 된 내용을 갱신해줍니다. 주로 실시간으로 내용이 추가되는 로그 파일을 모니터링할 때 사용합니다. |
| find | 특정 파일이나 폴더를 검색합니다. 파일명 혹은 폴더명, 확장자명으로 찾을 수 있습니다. |
| sudo | mac에서 설치가 안 되는 경우 보통 권한이 없어서 에러가 나는 경우가 많으므로 설치 명령어 앞에 sudo를 붙여 관리자 권한을 부여합니다. |
| ./ | ‘현재 폴더 안에 있는’ 이라는 뜻을 가지고 있으며, 생략할 수 있습니다. |
| ../ | 현 위치 바로 상위 폴더를 가르킵니다. |

- 설치순서

```jsx
1. "" 폴더 만들기
   => 이름은 영어로 작성해 주세요. (ex, frontend)

2. "" 폴더에 Next.js 프로젝트 설치하기
   => Next.js를 설치하면 React.js는 자동으로 함께 설치됩니다.
  npx create-next-app
  yarn add next@12.1.0 react@17.0.2 react-dom@17.0.2 --exact

3. "class" 폴더에 Emotion 설치하기
	yarn add @emotion/react
	yarn add @emotion/styled

4. "class" 폴더에 Apollo-Client, Graphql 설치하기
	yarn add @apollo/client graphql

5. "class" 폴더에 Ant-Design 설치하기
	yarn add antd

6. "class" 폴더에 Material-UI 설치하기
	yarn add @material-ui/core

7. "class" 폴더에 Axios 설치하기
	yarn add axios
```

### `React기초 및 폴더구조와 Emotion`

```jsx
01. index.html -> index.js
02. link href="" -> import styles from ""
```

### `포트폴리오 리뷰 - 폴더구조 및 emotion 적용`

```jsx
cmd + 클릭 -> 미리보기

제목 클릭 -> 전체보기

ctrl + - -> 전의 페이지로 이동

ctrl + shift + - -> 전의 페이지로 이동

멀티커서 + cmd + 방향키 -> 문장의 맨 끝
멀티커서 + cmd + shift + 방향키 -> 전체 드래그
```

### `React Component 및 state`

```jsx
state를 사용하는 이유: getElementByID같은 것을 사용하지 않아도 된다.
```

### `React실습`

- JS

```jsx
const onClickCountUp = () => {
	const count = Number(getElementById("count").innerText) +1;
	document.getElementById("count").innerText = count;
}

const onClickCountDown = () => {
	const count = Number(getElementById("count").innerText) -1;
	document.getElementById("count").innerText = count;
}

<div id="count">0</div>
<button onclick="onClickCountUp()">올리기</button>
<button onclick="onClickCountDown()">내리기</button>
```

- React

```jsx
import { useState } from 'react';
 

const [count, setCount] = useState(0);

const onClickCountUp = () => {
	setCount(count + 1);
}

const onClickCountDown = () => {
	setCount(count - 1);
}

<>
<div>{count}</div>
<button onClick={onClickCountUp}>올리기</button>
<button onClick={onClickCountDown}>내리기</button>
</>

setEmail(e.target.value)
```