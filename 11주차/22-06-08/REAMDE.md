2022년 6월 7일 화요일


# 자바 Spring 

- aop 복습

- 단위 테스트(Unit Test)
    - 구현 단계에서 각 모듈의 개발을 완료한 후 명세서의 내용대로 정확히 구현되었는지를 테스트하는 것
    - JUnit(Java), DBUnit(DB), CppUnit(C++), NUnit(.net), PyUnit(Python)
    - 장점
        - 개발단계 초기에 문제를 발결할 수 있게 도와줌
        - 리팩토링 또는 라이브러리 업그레이드 등에서 기능 확인을 도와줌(회귀 테스트)
        - 기능에 대한 불확실성 감소
        - 시스템에 대한 실제 문서 또는 예제로써 사용가능
        - 빠른 피드백과 기능을 안전하게 보호 가능
    
    - JUnit
        - Java의 단위테스트를 수행해주는 대표적인 Testing Framework
        - JUnit5 = JUnit Platform + JUnit Jupiter + JUnit Vintage
            - JUnit Platform : 테스트를 발견하고 테스트 계획을 생성하는 TestEngine 인터페이스를 가지고 있음. Platform은 TestEngine을 통해서 테스트를 발견하고 실행하고 결과를 보고.
            - JUnit Juptier : TestEngine의 실제 구현체는 별도 모듈인데 그중 하나. JUnit5에 새롭게 추가된 Jupiter API를 사용하여 테스트 코드를 발견하고 실행.
            - JUnit Vintage : 기존에 JUnit4 버전으로 작성한 테스트 코드를 실행할때 vintage-engine 모듈을 사용.
        -  JUnit Annotation
            - @Test : 해당 Method는 Test대상 메소드임을 의미한다.
            - @BeforeClass : 해당 테스트가 시작 전에 딱 한 번씩만 수행되도록 지정한다.
            - @AfterClass : 해당 테스트가 끝나고 딱 한 번씩만 수행되도록 지정한다.
            - @Before : 해당 테스트가 진행이 시작되기 전에 작업할 내용을 호출한다.
            - @After : 해당 테스트가 진행이 끝난 후에 작업할 내용을 호출한다.
            - @Ignore : TestCase를 무시할 수 있다.
