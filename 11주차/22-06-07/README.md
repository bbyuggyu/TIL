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

- AOP
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


