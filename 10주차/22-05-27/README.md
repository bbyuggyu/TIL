2022년 5월 27일 금요일


# 알고리즘 복습 AND 문제 풀이


트리 문제 이진트리

```java
import java.io.*;

public class n09934 {

	static int K;
	static int[] arr;
	static StringBuffer[] ans;

	public static void main(String[] args) throws Exception {

		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));

		K = Integer.parseInt(br.readLine());
		arr = new int[(int) Math.pow(2, K) - 1];

		String[] input = br.readLine().split(" ");
		for (int i = 0; i < arr.length; i++)
			arr[i] = Integer.parseInt(input[i]);

		ans = new StringBuffer[K];
		for (int i = 0; i < K; i++)
			ans[i] = new StringBuffer();

		solve(0, arr.length - 1, 0);

		for (int i = 0; i < K; i++)
			bw.write(ans[i].toString() + "\n");
		bw.flush();

	}

	public static void solve(int s, int e, int floor) {

		if (floor == K)
			return;

		int m = (s + e) / 2;
		ans[floor].append(arr[m] + " ");

		solve(s, m - 1, floor + 1);
		solve(m + 1, e, floor + 1);
	}

}
```


우선순위 큐 문제 가운데를 말해요

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.*;

public class Backjoon1655 {
    private static final BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

    public static void main(String[] args) throws IOException {
        int n = Integer.parseInt(br.readLine());
        StringBuilder sb = new StringBuilder();

        PriorityQueue<Integer> minHeap = new PriorityQueue<>((o1, o2) -> o1 - o2);
        PriorityQueue<Integer> maxHeap = new PriorityQueue<>((o1, o2) -> o2 - o1);

        for(int i = 0 ; i < n; i++){
            int num = Integer.parseInt(br.readLine());

            if(minHeap.size() == maxHeap.size()) maxHeap.offer(num);
            else minHeap.offer(num);

            if(!minHeap.isEmpty() && !maxHeap.isEmpty())
                if(minHeap.peek() < maxHeap.peek()){
                    int tmp = minHeap.poll();
                    minHeap.offer(maxHeap.poll());
                    maxHeap.offer(tmp);
                }

            sb.append(maxHeap.peek() + "\n");
        }
        System.out.println(sb);
    }
}
```