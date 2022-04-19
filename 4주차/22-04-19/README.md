2022년 4월 19일 화요일


# AOP: 백엔드 개발 필수

- Thread
    - process : 실행 중인 프로그램
    프로그램이 실행되면 OS로 부터 메모리를 할당받아 프로세스 상태가 됨
    - thread : 하나의 프로세스는 하나 이상의 thread를 가지게 되고, 실제 작업을 수행하는 단위는 thread임
    - multi-threading
        - 여러 thread가 동시에 수행되는 프로그래밍, 여러 작업이 동시에 실행되는 효과
        - thread는 각각 자신만의 작업 공간을 가짐 ( context )
        - 각 thread 사이에서 공유하는 자원이 있을 수 있음 (자바에서는 static instance)
        - 여러 thread가 자원을 공유하여 작업이 수행되는 경우 서로 자원을 차지하려는 race condition이 발생할 수 있음
        - 이렇게 여러 thread가 공유하는 자원중 경쟁이 발생하는 부분을 critical section 이라고 함
        - critical section에 대한 동기화( 일종의 순차적 수행)를 구현하지 않으면 오류가 발생할 수 있음

    - Thread 우선순위
        - Thread.MIN_PRIORITY(=1) ~ Thread.MAX_PRIORITY(=10)
        - 디폴트 우선순위 : Thread.NORMAL_PRIORITY(=5)
        - 우선 순위가 높은 Thread가 CPU의 배분을 받을 확률이 높다
        - setPriority()/getPriority()

    - join()
        - 동시에 두 개 이상의 Thread가 실행 될 때 다른 Thread의 결과를 참조 하여 실행해야 하는 경우 join() 함수를 사용
        - join() 함수를 호출한 Thread가 not-runnable 상태가 감
        - 다른 Thread의 수행이 끝나면 runnable 상태로 돌아옴
    - interrupt()
        - 다른 Thread에 예외를 발생시키는 interrupt를 보낸다.
        - Thread가 join(), sleep(), wait() 함수에의해 not-runnable 상태일 때 interrupt() 메서드를 호출하면 다시 runnable 상태가 될 수 있음
    
    - critical section 과 semaphore
        - synchronized
        - critical section  은 두 개 이상의 thread가 동시에 접근 하는 경우 문제가 생길 수 있기 때문에 동시에 접근할 수 없는 영역
        - semaphore 는 특별한 형태의 시스템 객체이며 get/release 두 개의 기능이 있다.
        - 한 순간 오직 하나의 thread 만이 semaphore를 얻을 수 있고, 나머지 thread들은 대기(blocking) 상태가 된다.
        - semaphore를 얻은 thread 만이 critical section에 들어갈 수 있다.

    - wait()/notify()
        - 리소스가 어떤 조건에서 더 이상 유효하지 않은 경우 리소스를 기다리기 위해 Thread 가 wait() 상태가 된다.
        - wait() 상태가 된 Thread은 notify() 가 호출 될 때까지 기다린다.
        - 유효한 자원이 생기면 notify()가 호출되고 wait() 하고 있는 Thread 중 무작위로 하나의 Thread를 재시작 하도록 한다.
        - notifyAll()이 호출되는 경우 wait() 하고 있는 모든 Thread가 재시작 된다.
        - 이 경우 유효한 리소스만큼의 Thread만이 수행될 수 있고 자원을 갖지 못한 Thread의 경우는 다시 wait() 상태로 만든다.
        - 자바에서는 notifyAll() 메서드의 사용을 권장한다.
        - notifyAll() 사용을 권장


# Java 프로그래밍 심화

- DBMS와 SQL
    - SQL 종류
        - DDL
            - 테이블 생성 CREATE 테이블이름 데이터타입(데이터크기) 제약조건
            - ALTER
            - DROP
        - DML
            - 데이터 등록 INSERT INTO 테이블이름(컬럼목록) VALUES(값목록);
            - 데이터 수정 UPDATE 테이블이름 SET 컬럼이름 = 수정값; (조건 WHERE)
            - 데이터 삭제 DELETE 테이블이름;
        - DQL
            - SELECT 컬럼이름;
            - FROM 테이블이름;
            - FROM 테이블이름;
        - DCL
        - TCL

        - 데이터타입
            - VARCHAR : 문자
            - NUMBER : 숫자
            - DATE : 날짜
        - 제약
            - PRIMARY KEY : 필수입력 AND 중복 불가능
            - NOT NULL : 필수입력

- JDBC
    - 자바에서 DB 프로그래밍을 하기 위해 사용되는 API (java.sql )
    - 다형성을 생각하면 됨

        
- 참고
    - scanner.(System.in)  
    키보드로부터 입력한 값을 라인 단위로 읽음
    - ORDER BY 컬럼이름 DESC; 내림차순  
    ASC: 오름차순
    