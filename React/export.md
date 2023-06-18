### export vs export Default

- export default

```jsx
파일명: qqq.js

const qqq = "도경"
export default qqq

-> 

import 아무거나 from './root/root/qqq.js

받아오는 파일의 기본값이 정해져 있기 때문에, 
받을 때 어떤 이름으로 받아도 상관이 없다.
```

- export

```jsx
파일명: qqq.js

const qqq = "도경"

export const zzz = "수지"

export const ccc = "지혜"

export const sss = "서로"

-> 

import { zzz, ccc } from './root/root/qqq.js

받아오는 파일의 변수를 골라서 가져올 수 있다.
```

- export 한 번에 하는 법

```jsx
import * as S from './root.styles.js
```

- export와 default를 한 번에 사용하는 법

```jsx
import qqq, { blueButton, RedInput } from "./root.js";
```