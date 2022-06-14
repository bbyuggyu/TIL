2022년 6월 14일 화요일


# 알고리즘 풀이

```java
/// 백준 11478 다른 부분 문자열의 개수
import java.util.*;

public class Main {

	static HashSet<String> set;

	public static void main(String[] args){

		Scanner sc = new Scanner(System.in);
		String s = sc.next();
		
		set = new HashSet<String>();
		
		String name = "";
		
		for(int i=0;i<s.length();i++) {
			name ="";
			for(int j=i;j<s.length();j++){
				name+=s.substring(j,j+1);
				set.add(name);
			}
		}
		
		System.out.println(set.size());
	}
}
```

# java spring mvc 구현