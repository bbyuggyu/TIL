2022년 8월 18일 목요일

# 알고리즘

- 탐욕알고리즘 문제

    - 잃어버린 기호 https://www.acmicpc.net/problem/1541
    ```java
    import java.io.BufferedReader;
    import java.io.ByteArrayInputStream;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.util.StringTokenizer;

    public class Main {
        public static void main(String[] args) throws IOException {
            String inputData = """
            00009-00009
            """;
            System.setIn(new ByteArrayInputStream(inputData.getBytes()));

            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            int result = 0;
            int subMaxMinus = 0;
            StringTokenizer subtraction = new StringTokenizer(br.readLine(),"-");
            StringTokenizer addition = new StringTokenizer(subtraction.nextToken(), "+");
            while (addition.hasMoreTokens()) {
                result += Integer.parseInt(addition.nextToken());
            }

            while (subtraction.hasMoreTokens()) {
                subMaxMinus = 0;
                addition = new StringTokenizer(subtraction.nextToken(), "+");
                while (addition.hasMoreTokens()) {
                    subMaxMinus += Integer.parseInt(addition.nextToken());
                }
                result -= subMaxMinus;
            }
            System.out.println(result);
        }
    }
    ```

    - 뒤집기 https://www.acmicpc.net/problem/1439
    ```java
    import java.io.BufferedReader;
    import java.io.ByteArrayInputStream;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.util.StringTokenizer;

    public class Main {
        public static void main(String[] args) throws IOException {
            String inputData = """
            11101101
            """;
            System.setIn(new ByteArrayInputStream(inputData.getBytes()));

            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            String S = br.readLine();
            StringTokenizer st1 = new StringTokenizer(S, "0");
            StringTokenizer st0 = new StringTokenizer(S, "1");
            System.out.println(Math.min(st0.countTokens(), st1.countTokens()));
        }
    }
    Main.main(new String[0]);
    ```

    - 시험감독 https://www.acmicpc.net/problem/13458
    ```java
    import java.io.BufferedReader;
    import java.io.ByteArrayInputStream;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.util.StringTokenizer;

    public class Main {
        public static void main(String[] args) throws IOException {
            String inputData = """
            5
            1000000 1000000 1000000 1000000 1000000
            5 7
            """;
            System.setIn(new ByteArrayInputStream(inputData.getBytes()));

            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            int N = Integer.parseInt(br.readLine());
            int[] A = new int[N];
            long count = 0;

            StringTokenizer st = new StringTokenizer(br.readLine());
            for (int i = 0; i < N; i++) {
                A[i] = Integer.parseInt(st.nextToken());
            }

            st = new StringTokenizer(br.readLine());
            int B = Integer.parseInt(st.nextToken());
            int C = Integer.parseInt(st.nextToken());

            for (int i = 0; i < N; i++) {
                if (A[i] >= B) {
                    A[i] -= B;
                    count += 1;

                    if (A[i] % C == 0) {
                        count += (A[i] / C);
                    } else {
                        count += (A[i] / C) + 1;
                    }
                } else {
                    count += 1;
                }
            }
            System.out.println(count);
        }
    }
    ```