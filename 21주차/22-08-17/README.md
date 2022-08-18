2022년 8월 17일 수요일

# 알고리즘

- 탐욕알고리즘 문제

    - 등수 매기기 https://www.acmicpc.net/problem/2012
    ```java
    import java.io.BufferedReader;
    import java.io.ByteArrayInputStream;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.util.Arrays;
    import java.util.StringTokenizer;

    public class Main {
        public static void main(String[] args) throws IOException {
            String inputData = """
            5
            1
            5
            3
            1
            2
            """;
            System.setIn(new ByteArrayInputStream(inputData.getBytes()));

            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            int N = Integer.parseInt(br.readLine());
            int[] rankings = new int[N];
            for(int i = 0; i < N; i++) {
                rankings[i] = Integer.parseInt(br.readLine());
            }
            Arrays.sort(rankings);

            long min = 0;
            for (int i = 0; i < N; i++) {
                min += Math.abs((i + 1) - rankings[i]);
            }
            System.out.println(min);
        }
    }
    ```

    - 주유소 https://www.acmicpc.net/problem/13305
    ```java
    import java.io.BufferedReader;
    import java.io.ByteArrayInputStream;
    import java.io.IOException;
    import java.io.InputStreamReader;
    import java.util.Arrays;
    import java.util.StringTokenizer;

    public class Main {
        public static void main(String[] args) throws IOException {
            String inputData = """
            4
            2 3 1
            5 2 4 1
            """;
            System.setIn(new ByteArrayInputStream(inputData.getBytes()));

            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
            int N = Integer.parseInt(br.readLine());

            long[] dists = new long[N - 1];
            StringTokenizer st = new StringTokenizer(br.readLine());
            for(int i = 0; i < N - 1; i++) {
                dists[i] = Long.parseLong(st.nextToken());
            }
            long[] prices = new long[N];
            st = new StringTokenizer(br.readLine());
            for (int i = 0; i< N; i++) {
                prices[i] = Long.parseLong(st.nextToken());
            }

            long minCost = dists[0] * prices[0];
            long minPrice = prices[0];
            for (int i = 1; i < N - 1; i++) {
                if (minPrice > prices[i]) {
                    minPrice = prices[i];
                }
                minCost += minPrice * dists[i];
            }
            System.out.println(minCost);
        }
    }
    ```