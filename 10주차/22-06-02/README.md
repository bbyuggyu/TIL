2022년 6월 2일 목요일


# 자바 Spring

<context:component-scan base-package="com.pastcampus.biz.user"/> 설정에서 중요한 포인트  
base-package로 지정한 패키지로 시작하는 모든 클래스를 스캔 범위에 포함시킨다.  
- com.pastcampus.biz  
- com.pastcampus.biz.user  
- com.pastcampus.biz.impl  
- com.pastcampus.biz.common  
  
  
참조변수 위에 @Autowired를 설정한 경우,  
- 해당 타입의 객체가 반드시 메모리에 있어야 하며,  
- 유니크하게 존재해만 한다.  
  
유지보수(운영) 과정에서 변경되는 객체는 XML 파일에 <bean> 등록한다.  
유지보수(운영) 과정에서 변경되지 않는 객체는 최대한 @Component를 적용한다.  
  
컴포넌트(Component)란?  
- 부품처럼 사용할 수 있는 소프트웨어 모듈  
- 일반적으로 소프트웨어 컴포넌트는 테이블 당 하나씩 작성하며, 테이블에 대한 CRUD 작업을 처리한다.  
- CRUD : Create(Insert), Read(Select), Update, Delete  
  
@Component  
    - @Service
    - @Repository
    - @Controller

@Autowired  
  
  
Servlet 게시판 Spring ioc 적용

