2022년 6월 7일 화요일


# 자바 Spring 

- AOP 설정
- Spring DAO
    - update() : INSERT, UPDATE, DELETE 명령어를 처리한다.
    - queryForInt() : 정수 하나를 검색하여 리턴한다.
    - queryForObject() : 검색 결과를 객체(Value Object) 하나에 매핑하여 리턴한다.
    - query() : 검색 결과 여러 개를 java.util.List에 저장하여 리턴한다. 
- DAO 클래스 구현

- Spring Swagger 
    - Open Api Specification(OAS)를 위한 프레임워크이다.
    - API들이 가지고 있는 스펙(spec)을 명세, 관리할 수 있는 프로젝트/문서
    - API 사용 방법을 사용자에게 알려주는 문서
    - Springboot에서 Swagger를 사용하면, 컨트롤러에 명시된 어노테이션을 해석하여 API문서를 자동으로 만들어준다.
    - 참고로 Swagger는 Java에 종속된 라이브러리가 아니다.
    - URL에 /swagger-ui.heml으로 접근하면 swagger가 만들어주는 페이지에 접근할 수 있다.

    - 기능
        - API Design (API 설계)
            - Swagger-editor를 통해 api를 문서화하고 빠르게 명세 가능
        - API Development
            - Swagger-codepen을 통해 작성된 문서를 통해 SDK를 생성하여 빌드 프로세스를 간소화할 수 있도록 도와준다.
        - API Documentation
            - Swagger-UI를 통해 작성된 API를 시각화시켜준다.
        - API Testing
            - Swagger-Inspector를 통해 API를 시각화하고 빠른 테스팅을 진행할 수 있다.
        - Standardize
            - Swagger-hub를 통해 개인, 팀원들이 API 정보를 공유하는 Hub

 