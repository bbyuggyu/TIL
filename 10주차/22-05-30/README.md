2022년 5월 30일 월요일


# 자바 Spring

- Spring
    - 자바 기반의 웹 어플리케이션을 만들 수 있는 프레임워크
    - JAVA 기술들을 더 쉽게 사용할 수 있게 해주는 오픈소스 프레임 워크
    - Spring 프레임워크는 POJO(Plain Old Java Object)를 기반으로 애플리케이션을 운용
    - 자바 객체와 라이브러리들을 관리해주며, 톰캣과 같은 WAS 가 내장되어 있어 자바 웹 어플리케이션을 구동
    - 객체의 생성 및 소멸과 같은 생명 주기(Life cycle)을 관리하며, Spring 컨테이너에서 필요한 객체를 가져와 사용
    - IOC와 DI
        - 제어의 역전 (IOC, Inversion Of Control)
            - 클래스 내부의 객체 생성 -> 의존성 객체의 메소드 호출이 아닌, 스프링에게 제어를 위임하여 스프링이 만든 객체를 주입 -> 의존성 객체의 메소드 호출 구조
        - 의존성 주입 (DI, Dependency Injection
            - 객체를 외부(Spring)에서 생성해서 사용하려는 주체 객체(A)에 주입시켜주는 방식

- Spring boot
    - Spring framework 기반 프로젝트를 복잡한 설정없이 쉽꼬 빠르게 만들어주는 라이브러리
    - 장점 
        - 라이브러리 관리 자동화.
        - 라이브러리 버전 자동관리
        - 설정 자동화
        - 내장Tomcat
        - 독립적으로 실행가능함 JAR
    - GET API
        - @RestController = Rest API 설정
        - @RequestMapping = 리소스 설정(method )
        - @GetMapping = Get Resource 설정
        - @RequestParam = URL Query Param Parsing
        - @PathVariable = URL Path Variable Parsing
        - @PostMapping = Post Resource 설정
        - @RequestBody = Request Body Parsing
        - @JsonProperty = json naming
        - @JsonNaming  = class json naming
        - @PutMapping = Put Resource\
        - @DeleteMapping = Delete Resource

- Framework
    - 뼈대
    - 아키텍처
    - 자주 쓰일 만한 기능들을 한데 모아 놓은 유틸(클래스)들의 모음(집합)
    - 기본적인 설계나 필요한 라이브러리는 알아서 제공해줄꺼니깐 개발자는 만들고 싶은 기능을 구현하는데 집중해라는 취지
    - 빠른 구현 시간 
    - 관리 용이성 증가
    - 개발자의 역량 획일화
    - 검증된 아키텍처의 재사용과 일관성 유지
    - MVC
        - MVC (모델-뷰-컨트롤러) 는 사용자 인터페이스, 데이터 및 논리 제어를 구현하는데 널리 사용되는 소프트웨어 디자인 패턴
        - Spring 프레임워크에 포함되어 있음
    - IoC
        - Inversion of Control
        - 제어의 역전
        - 메소드나 객체의 호출작업을 개발자가 결정하는 것이 아니라, 외부에서 결정되는 것
    - AOP
        - Aspect Oriented Programming
        - 관점 지향 프로그래밍
        - 여러 메서드에서 공통적으로 해야하는 일의 코드가 중복이 된다면 따로 모아서 관리를 하며 재활용을 하는것
        - 여러 메서드에서 사용되는것을 인터페이스로 구현을 하고 implements로 구현을 받게 된다.
    - Mybatis
        - 개발자가 작성한 SQL 명령어와 자바 객체(VO 혹은 DTO)를 매핑해주는 기능을 제공


참고 사이트 https://jerryjerryjerry.tistory.com/62