2022년 4월 21일 목요일


# AOP: 컴퓨터 공학 필수

- Quick Sort [퀵 정렬]
    - 하나의 리스트를 피벗(pivot)을 기준으로 두 개의 부분리스트로 나누어 하나는 피벗보다 작은 값들의 부분리스트, 다른 하나는 피벗보다 큰 값들의 부분리스트로 정렬한 다음, 각 부분리스트에 대해 다시 위 처럼 재귀적으로 수행하여 정렬하는 방법
    - 분할 정복(Divide and Conquer)
    - 비교 정렬
    - 데이터 외에 추가적인 공간을 필요로 하지 않는다. 제자리 정렬(in-place sort)
    - 불안정정렬(Unstable Sort)
    - 시간복잡도는 O(n log n)

- Merge Sort [합병/병합 정렬]
    - 문제를 분할하고, 분할한 문제를 정복하여 합치는 알고리즘
    - 분할 정복(Divide and Conquer)
    - 비교 정렬
    - 데이터 외에 추가적인 공간을 필요로 하기 때문에 제자리 정렬(in-place sort)이 아니다.
    - 구조상 최대한 작게 문제를 쪼개어 앞의 부분리스트부터 차례대로 합쳐나가기 때문에 안정정렬(Stable Sort)
    - 장점
        - 항상 두 부분리스트로 쪼개어 들어가기 때문에 최악의 경우에도 O(NlogN) 으로 유지가 된다.
        - 안정정렬이다.
    - 단정
        - 정렬과정에서 추가적인 보조 배열 공간을 사용하기 때문에 메모리 사용량이 많다.
        - 보조 배열에서 원본배열로 복사하는 과정은 매우 많은 시간을 소비하기 때문에 데이터가 많을경우 상대적으로 시간이 많이 소요된다.
    - 시간 복잡도 O(NlogN)


- 순차탐색
    - 탐색할 데이터가 모인 집합이 있으면 집합의 처음부터 끝까지 집합의 원소들을 비교하여 원하는 데이터를 찾는 알고리즘
    - 단방향으로 탐색을 진행하기 때문에 선형탐색(Linear Search)

- 이진탐색
    - 정렬된 배열 또는 리스트에 적합한 고속 탐색 방법
    - 배열의 중앙에 있는 값을 조사하여 찾고자 하는 항목이 왼쪽 또는 오른쪽 부분 배열에 있는지를 알아내어 탐색의 범위를 반으로 줄인다.
    - 찾고자 하는 값이 속해있지 않은 부분은 전혀 고려할 필요가 없기 때문에, 매 단계에서 검색해야 할 리스트의 크기를 반으로 줄일 수 있다.
    - 이러한 방법을 반복적으로 사용해 탐색하는 방법이 이진 탐색이다.
    - 데이터의 삽입이나 삭제가 빈번할 시에는 적합하지 않고, 주로 고정된 데이터에 대한 탐색에 적합하다.
    - 시간 복잡도 'T = K * logN'으로 O(logN)

- 그래프
    - 객체들이 쌍으로 연관되어 집합을 이루는 구조
    - 그래프의 구성 요소
        - 정점(Node, Vertex) - 객체, 위치의 개념
        - 간선(Edge) - 정점 간의 관계, 연결선(Link, Branch)
        - 인접 정점(Adjacent vertex) - 1개의 간선으로 직접 연결된 정점
        - 정점 차수(Degree) - 하나의 정점에 인접해 있는 간선의 개수
        - 진입 차수(In-Degree) - 방향성이 있는 그래프에서 외부에서 오는 간선의 수(내차수라고도 부른다)
        - 진출 차수(Out-Degree) - 방향성이 있는 그래프에서 외부로 향하는 간선의 수(외차수라고도 부른다)
        - 경로 길이(Path Length) - 정점에서 정점 간 경로 구성 시 사용된 간선의 수
        - 단순 경로(Simple Path) - 구성된 경로 중에서 반복되는 정점이 없는 경우
        - 사이클(Cycle) - 경로 중에서 시작 / 종료의 정점이 동일하여 내부적으로 순환이 발생하는 경우
    - 그래프 종류
        - 무방향 그래프
        - 방향 그래프
        - 가중치 그래프
        - 연결 그래프와 비연결 그래프
        - 사이클과 비순환 그래프
        - 완전 그래프
    
-  BFS 와 DFS
    - 너비 우선 탐색 (Breadth First Search): 정점들과 같은 레벨에 있는 노드들 (형제 노드들)을 먼저 탐색하는 방식
        - 한 단계씩 내려가면서, 해당 노드와 같은 레벨에 있는 노드들 (형제 노드들)을 먼저 순회함
        - 시간 복잡도: O(V + E)
    - 깊이 우선 탐색 (Depth First Search): 정점의 자식들을 먼저 탐색하는 방식
        - 한 노드의 자식을 타고 끝까지 순회한 후, 다시 돌아와서 다른 형제들의 자식을 타고 내려가며 순회함
        - 시간 복잡도: O(V + E) 





