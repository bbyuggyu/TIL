2022년 6월 10일 금요일


# 자바 Spring 

- 트랜잭션(Transaction)
    - 여러 작업을 진행하다가 문제가 생겼을 경우 이전 상태로 롤백하기 위해 사용
    - 더 이상 쪼갤 수 없는 최소 작업 단위
    - 랜잭션 커밋: 작업이 마무리 됨
    - 트랜잭션 롤백: 작업을 취소하고 이전의 상태로 돌림
    - Spring은 트랜잭션과 관련된 3가지 핵심 기술을 제공하고 있다. 그 3가지 핵심 기술은 다음과 같다.
        - 트랜잭션(Transaction) 동기화
            - 랜잭션을 시작하기 위한 Connection 객체를 특별한 저장소에 보관해두고 필요할 때 꺼내쓸 수 있도록 하는 기술
        - 트랜잭션(Transaction) 추상화
            - 트랜잭션 기술의 공통점을 담은 트랜잭션 추상화 기술
            - 종속적인 코드를 이용하지 않고도 일관되게 트랜잭션을 처리
        - AOP를 이용한 트랜잭션(Transaction) 분리
            - 해당 로직을 클래스 밖으로 빼내서 별도의 모듈로 만드는 AOP(Aspect Oriented Programming, 관점 지향 프로그래밍)
            - 트랜잭션 어노테이션(@Transactional)을 지원
    - 트랜잭션의 성질
        - 원자성(Atomicity) - 한 트랜잭션 내에서 실행한 작업들은 하나로 간주한다. 즉, 모두 성공 또는 모두 실패.
        - 일관성(Consistency)- 트랜잭션은 일관성 있는 데이타베이스 상태를 유지한다. (data integrity 만족 등.)
        - 격리성(Isolation) - 동시에 실행되는 트랜잭션들이 서로 영향을 미치지 않도록 격리해야한다.
        - 지속성(Durability) - 트랜잭션을 성공적으로 마치면 결과가 항상 저장되어야 한다.
    - 스프링에서는 트랜잭션 처리를 지원하는데 그중 어노테이션 방식으로 @Transactional을 선언하여 사용하는 방법이 일반적이며, 선언적 트랜잭션이라 부른다.
    -  스프링 트랜잭션 속성
        - isolation (격리수준)
            - DEFAULT
                - 기본 격리 수준(기본설정, DB의 Isolation Level을 따름)
            - READ_UNCOMMITTED (level 0)
                - 커밋되지 않는(트랜잭션 처리중인) 데이터에 대한 읽기를 허용
            - READ_COMMITTED (level 1)
                -  트랜잭션이 커밋 된 확정 데이터만 읽기 허용
            - REPEATABLE_READ (level 2)
                - 트랜잭션이 완료될 때까지 SELECT 문장이 사용하는 모든 데이터에 shared lock이 걸리므로 다른 사용자는 그 영역에 해당되는 데이터에 대한 수정이 불가능하다.
            - SERIALIZABLE (level 3)
                - 데이터의 일관성 및 동시성을 위해 MVCC(Multi Version Concurrency Control)을 사용하지 않음
                - 트랜잭션이 완료될 때까지 SELECT 문장이 사용하는 모든 데이터에 shared lock이 걸리므로 다른 사용자는 그 영역에 해당되는 데이터에 대한 수정 및 입력이 불가능하다.