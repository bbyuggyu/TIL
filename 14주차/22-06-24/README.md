2022년 6월 24일 금요일


# 컴퓨터 자료구조

- CPU 스케줄링 (CPU Scheduling)
    - 작업을 처리하기 위해서 프로세스들에게 CPU를 할당하기 위한 정책을 계획하는 것
    - 스케줄링 기준
        - CPU 이용률 (utilization)
        - 처리량 (throughput)
        - 총처리 시간 (turnaround time)
        - 대기 시간 (waiting time)
        - 응답 시간 (response time)
    - 스케줄링 알고리즘
        - 선입 선처리 (FCFS)
        - SJF (Shortest Job First)
        - RR (Round Robin)
        - 우선순위 스케줄링 (Priority Scheduling)
        - 다단계 큐 (Multilevel Queue) 스케줄링

- 프로세스 동기화
    - 여러 프로세스가 공유하는 자원의 일관성을 유지하는 것
    - 만일 두 개의 프로세스가 동시에 어떤 변수의 값을 바꿀 때 프로세스의 접근 순서에 따라 결과 값이 달라질 수 있는 상황을 경쟁 상태(Race Condition) 이라고 한다.
    - Critical Section(임계구역)
        - 멀티 프로세스 환경에서 둘 이상의 프로세스가 동시에 접근해서는 안되는 공유 자원의 코드 영역
    - 뮤텍스
        - 공유된 자원의 데이터를 여러 스레드가 접근하는 것을 막는 것입니다.
    - Semaphore(세마포어)
        - 두 개의 원자적 함수로 조작되는 정적 변수로써, 멀티 프로그래밍 환경에서 공유 자원(임계구역)에 대한 접근을 제한하는 방법
    - 