2022년 6월 13일 월요일


# 자바 Spring 퀴즈 제작

문제 1  
Servlet 컨테이너의 동작 순서로 올바른 것은?  
1. request - web.xml - servlet container - response  
2. request - servlet container - web.xml - response  
3. response - servlet container - web.xml - request   
4. response - web.xml - servlet container - request   
  
정답 : 1번  
해설 : 자바 Spring Container의 동작 순서는 클라이언트의 요청(request) - web.xml - servlet container생성 - 응답(request)이다.  
  
   
문제 2  
메소드 실행 전 사전처리 기능의 AOP 설정으로 반드시 필요한 어노테이션이 아닌 것은?  
  
1. @Component  
2. @Autowired  
3. @Before  
4. @Aspect  
  
정답 : 2  
해설 : @Autowired는 주로 변수 위에 설정하여 해당 타입의 객체를 찾아서 자동으로 할당하는 어노테이션이다.  
  
  
문제 3  
모든 메서드에서 예외가 발생할 때마다 Transaction이 실행되도록 코드를 작성하세요.  
  
```java
<!-- Transaction 설정 -->  
	<bean id="txManager" class="org.springframework.jdbc.datasource.DataSourceTransactionManager">  
		<property name="(1)" ref="dataSource"></property>  
	</bean>  
	
	<tx:advice id="txAdvice" transaction-manager="txManager">  
		<tx:attributes>
			<tx:method name="(2)" rollback-for="(3)"/>
		</tx:attributes>
	</tx:advice>
	
	<aop:config>
		<aop:pointcut id="txPointcut" expression="execution(* com.ssamz.biz..*Impl.*(..))" />
		<aop:(4) pointcut-ref="txPointcut" advice-ref="(5)"/>
	</aop:config>
```
  
정답 : (1) dataSource (2) * (3) Exception (4) advisor (5) txAdvice  
해설 : (1) DataSourceTransactionManager는 반드시 세터 인젝션으로 dataSource 객체를 할당해주어야 한다.  
         (2) 모든 경우를 표현할 때 사용하는 기호 *  
         (3) 예외 Exception   
         (4) Aspect로 Transaction 설정에서는 advisor를 사용  
         (5) id가 txAdvice로 설정된 Transaction을 관리  


- Spring MVC 적용