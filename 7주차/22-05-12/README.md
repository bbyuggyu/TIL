2022년 5월 12일 목요일


# AOP: 백엔드 개발 필수

- sql
    - 기본 문법
        - 데이터조회하기 (SELECT)
        - 테이블 구조 참조하기 (DESC)
        - 검색 조건 지정하기 (WHERE)
        - WHERE절 조건 조합하기
        - INSERT
        - UPDATE
        - DELETE
        - SELECT
        - view
        - 서브쿼리

    - 트랜잭션(Transaction)
        - 데이터베이스를 수정하거나 상태를 변화시키는 등의 작업을 수행하는 단위를 말한다.

        - 트랜잭션의 특징
            - 원자성 Atomicity
                - 깨지지 않는다. => 3개의 쿼리문이 원자처럼 하나로 묶여있다.
                - 트랜잭션이 모두 반영되거나, 아니면 전혀 반영되지 않아야 한다.
            - 일관성 Consistency
                - 데이터 결함과 관련.
                - 트랜잭션의 작업 처리 결과가 항상 일관성 있어야 한다.
            - 독립성 Isolation
                - 둘 이상의 트랜잭션이 실행되고 있을 경우, 어떤 특정 트랜잭션이라도 다른 트랜잭션에 끼어들 수 없다.
            - 지속성 : Durability
                - 트랜잭션이 성공적으로 완료되었을 경우, 결과는 영구적으로 반영되어야 한다.

        - 트랜잭션의 종류
            - 자동 커밋 트랜잭션(MSSQL디폴트) : 데이터 변경이 성공적으로 끝나면 자동으로 커밋 되고, 실패하면 자동으로 롤백된다.
            - 묵시적 트랜잭션(Oracle디폴트) : 자동 커밋 트랜잭션과 정 반대되는 개념이다.
            - 명시적 트랜잭션 : 사용자가 트랜잭션의 시작과 끝을 결정 짓는다. 명시적 트랜잭션을 사용하면 여러 데이터 변경 처리를 하나의 트랜잭션으로 묶어 처리할 수 있다.

        - 트랜잭션 격리 수준
            - Read Uncommitted
                - 트랜잭션 실행 중 다른 트랜잭션이 접근 가능(트랜잭션이 격리되지 않음)
                - A트랜잭션이 데이터를 변경 중 일 때 B트랜잭션이 접근하여 커밋되기전 변경된 데이터를 읽을 수 있음.
                - 만약 커밋되지 않고 A트랜잭션이 롤백되면 B트랜잭션의 결과값은 잘못된 데이터가 됨(Dirty Read 발생)
                - Non-Repeatable Read 발생 가능
                - Phantom Read 발생 가능
            - Read Committed
                - 커밋되기 전 바뀐 데이터를 읽을 수 없음.(Dirty Read 발생 X)
                - Non-Repeatable Read 발생 가능
                - Phantom Read 발생 가능
            - Repeatable Read 
                - 항상 한 트랜잭션의 일관성 있는 데이터 읽기를 보장(Dirty Read, Non-Repeatable Read 발생 X)
                - A트랜잭션 실행 중 B 트랜잭션에서 Insert가 발생 후 동일 조건의 Select문의 A트랜잭션과 B트랜잭션의 결과가 달라짐(Phantom Read 발생)
                - A트랜잭션이 실행 중일 때 다른 트랜잭션이 DB의 내용을 변경해도 서로 영향을 미치지 않는다.
            - Serializable
                - 가장 높은 격리 수준
                - 트랜잭션이 완료될 때까지 Select 문장이 사용하는 모든 데이터에 Shared Lock이 걸리므로 다른 트랜잭션이 접근 불가
                - Dirty Read, Non-Repeatable Read, Phantom Read 모두 발생 안함.


# 자바 SERVLET

- 데이터 베이스 연동
- 핵심 API
    - HttpServletRequest 메소드
    - HttpServletResponse 메소드
- 로그인 인증 처리