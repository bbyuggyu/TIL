2022년 4월 12일 화요일


# 권장강의

- 자바스크립트
    - 자료형
    - 조건문
    - 반복문
    - 함수


# AOP: 백엔드 개발 필수

- 배열
    - 동일한 자료형의 순차적 자료 구조
    - 인덱스 연산자[]를 이용하여 빠른 참조가 가능
    - 물리적 위치와 논리적 위치가 동일
    - 배열의 순서는 0부터 시작
    - 자바에서는 객체 배열을 구현한 ArrayList를 많이 활용함
    - 배열의 선언
        - ```java
            int[] arr1 = new int[10];
            int arr2[] = new int[10];
            ``` 
    - 배열의 초기화
        - ```java
            int[] numbers = new int[] {10, 20, 30};  //개수 생략해야 함
            int[] numbers = {10, 20, 30};            // new int[]  생략 가능 
            int[] ids; 
            ids = new int[] {10, 20, 30};            // 선언후 배열을 생성하는 경우는 new int[] 생략할 수 없음
            ```
    - 배열을 선언하면 개수만큼 메모리가 할당되지만, 실제 요소(데이타)가 없는 경우도 있음
    - 배열의 length 속성은 배열의 개수를 반환해주기 때문에 요소의 개수와는 다름

- 객체 배열
    - 기본 자료형 배열은 선언과 동시에 배열의 크기만큼의 메모리가 할당되지만,  
      객체 배열의 경우엔 요소가 되는 객체의 주소가 들어갈(4바이트, 8바이트) 메모리만 할당되고(null) 각 요소 객체는 생성하여 저장해야 함
    - System.arrayCopy(src, srcPos, dest, destPos, length) 자바에서 제공되는 배열 복사 메서드
        - 얕은 복사
        - 깊은 복사

- 다차원 배열
    - 이차원 이상으로 구현 된 배열
    - 평면 (이차원 배열) 이나 공간(삼차원 배열)을 활용한 프로그램 구현
    - 다차원 배열 선언
        - ```java
            int[][] arr = {{1,2,3}, {4,5,6}}
          ```

- ArrayList
    - 기존의 배열 선언과 사용 방식은 배열의 길이를 정하고 요소의 개수가 배열의 길이보다 커지면 배열을 재할당하고 복사해야 했음
    - 배열의 요소를 추가하거나 삭제하면 다른 요소들의 이동에 대한 구현을 해야 함
    - ArrayList는 객체 배열을 좀더 효율적으로 관리하기 위해 자바에서 제공해 주는 클래스
    - 이미 많은 메서드들이 최적의 알고리즘으로 구현되어 있어 각 메서드의 사용 방법만 익히면 유용하게 사용할 수 있음
    - 한번 생성되면 크기가 변하지 않는 배열과는 달리 ArrayList는 객체들이 추가되어 저장 용량을 초과한다면 자동으로 부족한 크기만큼 저장 용량이 늘어난다


# JAVA 프로그래밍 심화

- 추상 메소드
    - 추상 클래스는 키워드 ```abstract```를 붙여 표현한다.
    - 추상 메서드를 포함하지 않은 클래스에서도 ```abstract```를 붙여서 추상 클래스로 지정할 수도 있다.
    - 클래스를 abstract로 지정하면 ```new```를 통해 객체를 직접 생성할 수 없다.
    - 메소드에 abstract를 사용할 경우 interface의 메소드와 같이 구현 부분은 없다.
    - abstract로 선언한 메소드를 자식 클래스에서 반드시 구현해야 한다. (오버라이딩)
    - 이는 자식 클래스에서 추상 메서드를 반드시 구현하도록 강제하는 것이다.

- 인터페이스
    - 추상 클래스처럼 불완전한 것이기 때문에 그 자체만으로 사용되기 보다, 다른 클래스를 작성하는데 도움을 줄 목적으로 작성된다.
    - 일반 메서드 또는 멤버 변수를 구성원으로 가질 수 없다.
    - 모든 멤버 변수는 ```public static final```이어햐 하며, 이를 생략할 수 있다.
    - 모든 메서드는 ```public abtract```이어야 하며, 이를 생략할 수 있다.  
      (단, JDK1.8부터 static 메서드와 default 메서드를 사용할 수 있다.)
    - 인터페이스는 인터페이스로부터만 상속받을 수 있으며, 클래스와 달리 다중상속을 받는 것이 가능하다.
        - 상속 명령어 implements

- 예외
    - try ~ catch
    - 다중 catch
    - Exception 예외처리는 마지막에
    - finally : 예외 발생 여부와 무관하게 무조건 실행
    - throws : 예외 처리를 부모에게 넘김

