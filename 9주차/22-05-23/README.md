2022년 5월 23일 월요일


# 자바 jsp

- JSP (JavaServer Pages )
    - HTML 코드에 JAVA 코드를 넣어 동적웹페이지를 생성하는 웹어플리케이션 도구
    - JSP 가 실행되면 자바 서블릿(Servlet) 으로 변환되며 웹 어플리케이션 서버에서 동작되면서 필요한 기능을 수행하고 그렇게 생성된 데이터를 웹페이지와 함께 클라이언트로 응답
    -  JSP 태그
        |구분|태그|내용|
        |:---:|:---:|:---:|
        |주석|<%--  --%>|주석 처리|
        |지시자|<%@    %>|페이지 속성 지정|
        |스크립트릿|<%!     %>|JAVA 코드 삽입|
        |표현식|<%!     %>|결과값 출력|
        |선언|<%!     %>|변수, 메소드의 선언|
    - 내장 객체
        - JSP 내에서 선언하지 않고 사용할 수 있는 객체
            - request
            - response
            - out
            - session
            - config
            - application
            - exception
        - 내장객체와 정보 공유
            - request < session < application
