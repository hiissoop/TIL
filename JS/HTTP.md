### HTTP 

- Hypertext Transfer Protocol (서버와 클라이언트가 통신하기 위해 정의된 규약)
- 작동방식
    1. 사용자가 (GET,POST)로 서버에 요청한다. (Request Body) 
    2. GET/경로/HTTP버전/HOST URL정보/User-Agent 브라우저정보/Accept-Language/ (Request Body)
    3. 서버가 응답한다. (Response Body)
    4. HTTP버전/200 성공여부/Content-Type JSON객체/ (Response Body)

- Request
    - GET: 서버의 데이터를 조회하는 Method (request body x)
    - POST: 서버에 데이터를 등록하는 Method (request body o)
    - PUT: 서버 내 데이터를 수정하는 Method
    - PATCH: 데이터를 일부 수정하는 Method
    - DELETE: 서버의 데이터를 삭제하는 Method
    - OPTIONS: 서버가 허용하는 Method를 확인하기 위한 Method