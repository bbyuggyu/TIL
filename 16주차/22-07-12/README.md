2022년 7월 12일 화요일


# 자바 스프링부트

- 스프링시큐리티(Spring Security)
    - 스프링 기반의 애플리케이션의 보안(인증과 권한, 인가 등)을 담당하는 스프링 하위 프레임워크
    - 서블릿 필터(filter)와 이들로 구성된 필터체인으로의 구성된 위임모델을 사용
    - 기본용어
        - 접근 주체(Principal) : 보호된 리소스에 접근하는 대상
        - 인증(Authentication) : 보호된 리소스에 접근한 대상에 대해  누구인지, 애플리케이션의 작업을 수행해도 되는 주체인지 확인하는 과정(ex. Form 기반 로그인) => 즉, 누구인지?
        - 인가(Authorize) : 해당 리소스에 대해 접근 가능한 권한을 가지고 있는지 확인하는 과정(After Authentication, 인증 이후)  => 즉, 어떤 것을 할 수 있는지?
        - 권한 : 어떠한 리소스에 대한 접근 제한, 모든 리소스는 접근 제어 권한이 걸려있음. 인가 과정에서 해당 리소스에 대한 제한된 최소한의 권한을 가졌는지 확인
    - 특징과 구조 
        - 보안과 관련하여 체계적으로 많은 옵션을 제공하여 편리하게 사용할 수 있음
        - Filter 기반으로 동작하여 MVC와 분리하여 관리 및 동작 
        - 어노테이션을 통한 간단한 설정
        - Spring Security는 기본적으로 세션 & 쿠키방식으로 인증
        - 인증관리자(Authentication Manager)와 접근 결정 관리자(Access Decision Manager)를 통해 사용자의 리소스 접근을 관리
        - 인증 관리자는 UsenamePasswordAuthenticationFilter, 접근 결정 관리자는 FilterSecurityInterceptor가 수행