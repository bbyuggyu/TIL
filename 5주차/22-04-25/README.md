2022년 4월 25일 월요일


# AOP: 컴퓨터 공학 필수

- 프림 알고리즘
    - 정점 선택 기반의 알고리즘으로, 하나의 정점에서 연결된 간선들 중에 최소 간선 비용을 가진 정점을 하나씩 선택하면서 MST를 찾는 알고리즘
    - 무방향 그래프
    - 인접한 정점 중 최소비용으로 이동가능한 정점을 선택하면서 방문하는 알고리즘
    - 크루스칼 알고리즘과 같은 용도지만, 응용상황에 따라 두 알고리즘의 효율성이 달라질 수 있다.
    - 크루스칼 알고리즘과의 차이는 간선을 기준으로 하는것이 아닌 정점을 기준으로 판단하는 것이다.
    - 프림 알고리즘 동작 과정
        1. 임의의 정점 하나를 선택해서 시작합니다.
        2. 선택한 정점과 인접하는 정점들 중에 최소 비용의 간선을 가지는 정점을 선택합니다.
        3. 모든 정점이 선택될 때까지 반복합니다.
        프림의 경우 선택된 정점들과 연결된, 선택되지 않은 정점들의 간선에서 최소 간선 비용을 가진 정점을 선택하는 방식으로 진행
    - 시간복잡도 O(ElogV)

- 자바 입출력 스트립
    - ```java 
        FileReader reader = new FileReader("파일명");
		BufferedReader buffReader = new BufferedReader(reader);
		
		FileWriter writer = new FileWriter("파일명");
		BufferedWriter buffWriter = new BufferedWriter(writer);
        ```
- Properties 
