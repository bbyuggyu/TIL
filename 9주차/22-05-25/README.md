2022년 5월 25일 수요일


# 자바 jsp

자바 jsp 검색 기능 구현 연습  
model2 적용 연습  
el과 jstl 적용하여 코드 작성 연습


# 알고리즘 복습

링크드리스트 복습 및 문제 풀이

```java
Scanner scanner = new scanner(System.in)
int n = scanner.nextInt();
int m = scanner.nextInt();

List<Integer> A = new ArrayList<>();
for (int i = 0; i < n; i++) {
    int n = scanner.nextInt();
    A.add(n);
}

List<Integer> B = new ArrayList<>();
for (int i = 0; i < m; i++) {
    int n = scanner.nextInt();
    B.add(n);
}

List<Integer> result = new ArrayList<>();
int i = 0, j = 0;
while(i < n || j < m) {
    int a = A.get(i);
    int b = B.get(i);

    if (a <=b) {
        result.add(a);
        i++
    } else {
        result.add(b);
        j++
    }
}
for (; i < n; i++) {
    result.add(A.get(i))
}
for (; j < n; j++) {
    result.add(A.get(j))
}

StringBuilder sb = new StringBuilder();
for (ine e : result) {
    sb.append(e + " ");
}
System.out.println(sb.toString());
```