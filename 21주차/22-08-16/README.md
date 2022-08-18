2022년 8월 16일 화요일

# 알고리즘

- 탐욕알고리즘 문제

    - 동전 https://www.acmicpc.net/problem/11047
    ```java
    import java.io.BufferedReader;
    import java.io.ByteArrayInputStream;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.util.*;
    public class Main {
        public static void main(String[] args) throws IOException {
            String inputData = “”"
            10 4200
            1
            5
            10
            50
            100
            500
            1000
            5000
            10000
            50000
            “”";
            System.setIn(new ByteArrayInputStream(inputData.getBytes()));
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            StringTokenizer st = new StringTokenizer(br.readLine());
            int N = Integer.parseInt(st.nextToken());
            int K = Integer.parseInt(st.nextToken());
            Integer[] coins = new Integer[N];
            for (int i = 0; i < N; i++) {
                coins[i] = Integer.parseInt(br.readLine());
            }
            Arrays.sort(coins, Collections.reverseOrder());
            int count = 0;
            for (int i = 0; i < N; i++) {
                if (K >= coins[i]) {
                    count += (K / coins[i]);
                    K %= coins[i];
                    if (K <= 0) {
                        break;
                    }
                }
            }
            System.out.println(count);
        }
    }
    ```

    - ATM https://www.acmicpc.net/problem/11399
    ```java
    import java.io.BufferedReader;
    import java.io.ByteArrayInputStream;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.util.Arrays;
    import java.util.Collections;
    import java.util.StringTokenizer;

    public class Main {
        public static void main(String[] args) throws IOException {
            String inputData = """
            5
            3 1 4 3 2
            """;
            System.setIn(new ByteArrayInputStream(inputData.getBytes()));

            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            int N = Integer.parseInt(br.readLine());
            StringTokenizer st = new StringTokenizer(br.readLine());
            int[] minutes = new int[N];
            for (int i = 0; i < N; i++) {
                minutes[i] = Integer.parseInt(st.nextToken());
            }
            Arrays.sort(minutes);
            int min = 0;

            for (int i = 0; i < N; i++) {
                for (int j = 0; j < i + 1; j++) {
                    min += minutes[j];
                }
            }
            System.out.println(min);
        }
    }
    ```