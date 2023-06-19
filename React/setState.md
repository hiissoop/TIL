### setState 동작원리

```jsx
import { useState } from 'react' 

export default function counterStatePage() {
    const [count, setCount] = useState(0);

    const qqq = Math.random(); 
    console.log(qqq);

    const onClickCountUp = () => {
        setCount(1)       // 임시저장
        setCount(2)       // 임시저장
        setCount(3)
        setCount(4)
        setCount(5)
        setCount(6)       // 마지막 저장 후 리렌더링
    }
    return (
        <div>
            <div>{count}</div>
            <button onClick={onClickCountUp}>카운트 올리기</button>
        </div>
    );
}
```