2022년 6월 7일 화요일


# 알고리즘 문제 풀이

- 1929 소수 구하기

```java 
import java.util.Scanner;

public class Main {
	public static boolean[] prime;
	public static void main(String[] args) {
 
		Scanner in = new Scanner(System.in);
		int M = in.nextInt();
		int N = in.nextInt();
		
		prime = new boolean[N + 1];
		get_prime();
				
		for(int i = M; i <= N; i++) {
			// false = 소수 
			if(!prime[i]) System.out.println(i);
		}
	}
 
 
	// 에라토스테네스의 체 알고리즘
	public static void get_prime() {
		// true = 소수아님 , false = 소수 
		prime[0] = prime[1] = true;
		
		for(int i = 2; i <= Math.sqrt(prime.length); i++) {
			if(prime[i]) continue;
			for(int j = i * i; j < prime.length; j += i) {
				prime[j] = true;
			}
		}
	}
}
```


# 자바 Spring


AOP(Aspect Oriented Programming) : 관심지향 프로그래밍

XXXServiceImpl 클래스가 비즈 니스 클리스다. 
비즈니스 클래스에는 비즈니스 메소드가 구현되어있으며, 비즈니스 메소드가 가진 코드가 핵심 관심 코드다.

XXXAdvice 클래스가 횡단관심 클래스다. 
횡단관심 클래스에는 비즈니스 메소드마다 실행될 공통의 로직이 들어있으며, 공통 로직이 횡단관심 코드다.

AOP 용어
Pointcut : 필터링된 조인포인트(= 비즈니스 메소드)

리턴 타입 필터링
- * : 모든 리턴 타입을 허용한다.
- void : 리턴 타입이 void인 메소드만 필터링한다.
- !void : 리턴 타입이 void가 아닌 메소드만 필터링한다.

패키지 경로 필터링
- com.ssamz.biz.board : 정확하게 com.ssamz.biz.board인 패키지를 필터링한다.
- com.ssamz.biz.. : com.ssamz.biz로 시작하는 모든 패키지를 필터링한다.
- com.ssamz..board : com.ssamz로 시작하는 모든 패키지 중에서 패키지 마지막이 
                            board인 패키지를 필터링한다.

클래스 이름 필터링
- BoardServiceImpl : BoardServiceImpl 클래스를 필터링한다.
- *Impl : 클래스 이름이 Impl로 끝나는 모든 클래스(XXXImpl)

메소드 이름 필터링
- getBoardList : 이름이 정확하게 getBoardList 인 메소드 필터링
- get* : 이름이 get으로 시작하는 모든 메소드(get())도 포함

매개변수 필터링
(..) : 모든 경우의 매개변수의 갯수와 타입을 허용한다.


Advice : 횡단 관심에 해당하는 공통 기능의 코드
어드바이스 동작 시점을 5가지(before, after, after-returning, after-throwing, around)로 지정 

Aspect(= Advisor) : Pointcut + Advice


- 관심 분리(Separation of Concerns)
- 횡단 관심(Crosscutting Concerns)
- 핵심 관심(Core Concerns)
- 조인포인트(Joinpoint)
- 포인트컷(Pointcut)
	- 필터링된 조인포인트 
- Pointcut 설정 
- 어드바이스(Advice)
	- Before
	- After Returning
	- After Throwing
	- After
	- Around
- 애스팩트(Aspect)
	- 포인트컷과 어드바이스의 결합


