2022년 5월 31일 화요일


# 자바 Spring

lazy-loading : 클라이언트의 요청이 들어올 때 까지 객체 생성을 늦춘다.  
pre-loading : 컨테이너가 생성될 때 XML에 등록된 클래스의 객체를 생성한다.  
  
Servlet : lazy-loading  
Filter, Listener : pre-loading  
  
스프링 컨테이너(GenericXmlApplicationContext)는 XML에 등록된 객체를 Pre-loading한다.  
스프링 컨테이너는 객체를 생성할 때 기본 생성자만 호출한다.  
스프링 컨테이너는 XML에 등록된 순서대로 객체를 생성한다.  
  
IoC(Inversion of Control) : 제어의 역전(역제어 <---> 순제어)  
어플리케이션 운용에 필요한 객체의 생성과 객체들 간의 의존관계를 자바 코드가 아닌   
컨테이너가 모두 처리하는 것  
  
XML 파일에 새로운 네임스페이스를 추가한다는 것은 스프링 컨테이너에게 전혀 다른   
종류의 작업을 지시할 수 있음을 의미한다.  
  
<bean> 태그에서 id는 생략 가능하다. 하지만  class 속성은 필수다.  
id를 통해 생성된 객체를 식별할 수 있어야 하기 때문에  
id 속성 값을 반드시 전체 객체에서 유일해야 한다.  
id 속성 값은 자바의 변수명 규칙을 적용한다.  
  
모든 컨테이너는 컨테이너가 종료되기 직전에 컨테이너가 생성한 객체들을 먼저   
메모리에서 제거하는 작업을 수행한다.  
  
lazy-init="true" 는 특정 객체를 Pre-loading이 아닌 Lazy-loding으로 생성하도록한다.  
디폴트는 lazy-init="false"다.  
  
scope="prototype"은 특정 객체를 요청(getBean()) 할때마다 새로운 객체를 생성하여 리턴한다.  
scope="singleton"이 디폴트 설정이며, 하나의 객체만 유지한다.  
  
생성자 인젝션은 <constructor-arg> 태그를 이용하여 생성자를 호출한다.   
세터 인젝션은 <property> 태그를 이용하여 세터 메소드를 호출한다.  
  
<bean class="polymorphism.SonySpeaker"/> --> polymorphism.SonySpeaker#0  
@Component                               --> 클래스 이름의 첫 글자를 소문자로(lgTV)
