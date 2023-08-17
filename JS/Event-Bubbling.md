### 이벤트 버블링

- 자식에서 부모로 전파되는 방식 (자식의 함수 실행 → 부모의 함수 실행 → 부모의 함수 실행)
    - [event.target.id](http://event.target.id) / [event.currentTarget.id](http://event.currentTarget.id) /
    - event.stopPropagation() // 상위 이벤트가 실행되는 걸 막는다.