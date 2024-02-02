- ERD / API
  
https://receptive-platinum-aea.notion.site/ERD-API-736e64979ece49b5a10a0dc95df3e171?pvs=4

< Q / A >

암호화 <br>
해시 함수는 단방향 암호화애 사용되며, 원래의 값을 해시 값으로 변환하는 건 가능하나, 해시 값을 원래의 값으로 돌리는 건 어려우므로 원래 비밀번호를 추론할 수 없어 보안에 도움이 된다.


인증 방식<br>
토큰이 조작되거나 탈취될 가능성이 있으므로, 토큰에 최소한의 정보만을 포함시키고, 토큰의 만료시간을 짧게 설정하여 만료가 되면 새로운 토큰을 발급하도록 한다.

인증과 인가<br>
인증은 사용자의 신원을 확인하는 단계이며, 인가는 해당 리소스에 대해 권한 여부를 확인한다. 과제의 미들웨어는 인증에 해당한다.

Http Status Code <br>
200 : OK → 응답 성공, 주로 get 요청의 응답 <br>
201 : Created → 리소스 생성, 주로 post 요청의 응답 <br>
400 : Baed Request → 클라이언트의 잘못된 요청, 주로 인증 실패 시 응답 <br>
404 : Not Found → 클라이언트가 요청한 url 에 리소스가 없을 경우 <br>
409 : Confilct → 클라이언트가 요청한 리소스와 서버의 리소스 간의 충돌/중복이 발생한 경우  <br>

리팩토링<br>
MySQL 은 관게형 데이터베이스이며 MongoDB는 NoSQL 데이터베이스다.  <br>
Prisma 와 TypeORM 도 서로 다른 방식으로 쿼리를 제공하기 떄문에 전환 시 변경해야할 코드 규모가 클 것이다.  <br>
코드 변경을 최소화하기 위해서는 추상화와 모듈화가 중요하다고 생각한다. <br>

API 명세서<br>
자동으로 문서화가 되고, 엔드포인트를 직접 테스트할 수 있어서 협업에 좋다. 
