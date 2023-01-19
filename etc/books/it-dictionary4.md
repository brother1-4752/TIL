# EP22-25

# EP22 자료구조와 알고리즘

- **개발자가 알고리즘과 자료구조를 왜 배워야 할까?**
    
    ```html
    개발자들은 알고리즘과 데이터 구조를 배워야 한다. 왜냐하면 그것들은 **특정 문제를 보다 효율적이고 효과적으로 해결할 수 있는 방법을 제공**하기 때문이다. 예를 들어, 개발자는 대규모 데이터 세트에서 특정 데이터 조각을 찾아야 할 수 있으며, **이진 탐색**과 같은 검색 알고리즘을 사용하면 선형 검색과 같은 다른 방법에 비해 해당 데이터를 찾는 데 필요한 시간을 크게 줄일 수 있다. 또한 **링크드 리스트와 해시 테이블과 같은 데이터 구조**를 이해하면 개발자가 특정 작업에 대한 데이터를 저장하고 구성하기에 가장 좋은 구조를 선택할 수 있으므로 성능과 확장성이 향상된다.
    ```
    
- **패스파인더 알고리즘**
    
    ```html
    Dijkstra's algorithm is still widely used today in a variety of applications, such as routing and network design, due to its simplicity and its ability to handle graphs with non-negative edge weights. However, there have been many improvements and variations of Dijkstra's algorithm developed over the years.
    
    One example is the A* (A-star) algorithm which is an extension of Dijkstra's algorithm that incorporates a heuristic function to guide the search, making it more efficient when the goal is known. A* algorithm is commonly used in pathfinding and robotics
    
    Another example is the Bidirectional Dijkstra's algorithm, which simultaneously searches from the start and goal node, meeting in the middle, reducing the search time.
    
    Additionally, there are other pathfinding algorithm like Bellman-Ford, Floyd-Warshall, and Johnson algorithm that might be considered based on the scenario.
    
    It's important to note that the choice of algorithm depends on the specific problem and constraints of the application, so it's important to understand the trade-offs between different algorithms and choose the one that best fits the needs of the project.
    ```
    
- **압축 알고리즘**
    
    ```html
    압축 알고리즘은 저장 공간을 절약하고 데이터 전송에 걸리는 시간을 줄이기 위해 데이터 크기를 줄이는 데 사용되는 방법입니다. 압축 알고리즘의 일반적인 유형은 다음과 같다:
    
    무손실 압축 알고리즘: 이러한 알고리즘은 압축된 데이터에서 원본 데이터를 완전히 재구성할 수 있는 방식으로 데이터를 압축합니다. 예를 들어 허프만 코딩과 렘펠-지브-웰치(LZW) 압축이 있다.
    
    손실 압축 알고리즘: 이러한 알고리즘은 일부 정보를 제거하여 데이터를 압축하므로 품질이 저하됩니다. 예로는 JPEG 이미지 압축에 사용되는 이산 코사인 변환(DCT)과 MP3 오디오 압축에 사용되는 푸리에 변환이 있다.
    
    실행 길이 인코딩(RLE): 이것은 연속적으로 반복되는 요소를 요소의 단일 복사본과 반복 횟수로 대체하는 간단한 압축 알고리즘입니다.
    
    버로우스-휠러 변환(BWT): 이것은 bzip2와 같은 다른 압축 알고리즘의 전처리 단계로 사용되는 압축 알고리즘으로, 반복되는 문자의 실행을 더 많이 포함하도록 데이터를 재정렬하여 압축성을 향상시킨다.
    
    산술 코딩: 이것은 0과 1 사이의 단일 숫자로 기호의 문자열을 표현하는 것을 기반으로 하는 압축 알고리즘으로, 이것은 기호를 표현하기 위해 비트의 분수를 사용할 수 있게 하고 다른 무손실 알고리즘보다 더 효율적일 수 있다.
    
    알고리즘의 선택은 응용 프로그램의 특정 문제와 제약 조건에 따라 달라지므로 서로 다른 알고리즘 간의 균형을 이해하고 프로젝트의 요구에 가장 적합한 알고리즘을 선택하는 것이 중요합니다.
    ```
    
- 자료구조는 데이터를 효율적으로 보관하고 찾기 위한 자료 구조입니다. 프론트엔드 개발자가 된다면, 백엔드에서 내려받은 JSON 데이터로 그것을 보기 좋게 화면에 띄우는 역할을 한다. 이 때, 데이터가 산발적으로 흩어져 있으면, 찾는데 오래 걸릴 것이다. 그렇기 때문에 보기 좋게 보관을 잘 해야 한다. 이러한 이유로 우리는 자료구조를 배웁니다.
- 자료구조에도 여러 가지 방식이 있다. 데이터를 작은 것부터 큰 순서로 정리하는 자료구조(데이터 크기 기준), 이름표를 붙여서 정리하는 자료구조(검색을 위한 인덱스 기준), 데이터가 들어오는 순서로 정리하는 자료구조(생성 시간 기준) 등 매우 다양하다.

# 왜 자료구조는 다양할까?

- 프로그램의 목적이 다양하기 때문이다.

# EP23 배열

- 시간복잡도는 작업 속도
- 램은 주소지가 적힌 박스가 많이 있는 창고라고 생각하면 됩니다. 박스에는 데이터를 1개씩 저장할 수 있고, 박스마다 주소가 각각 있다. 그러면 박소에 보관된 데이터를 빠르게 찾을 수 있다.

# EP24 알고리즘의 속도는 어떻게 표현할까?

```html
알고리즘의 속도는 일반적으로 입력 데이터 크기의 함수로 알고리즘이 실행되는 데 걸리는 시간을 설명하는 시간 복잡성 측면에서 표현된다. 시간 복잡성을 표현하는 가장 일반적인 방법은 알고리즘의 실행 시간의 상한을 설명하는 큰 O 표기법을 사용하는 것이다.

예를 들어, 시간 복잡도가 O(n)인 알고리즘은 입력 데이터의 크기가 커질수록 선형적으로 더 많은 시간이 걸리는 반면, 시간 복잡도가 O(log n)인 알고리즘은 입력 데이터의 크기가 커질수록 로그적으로 더 많은 시간이 걸린다.

시간 복잡성을 표현하는 또 다른 방법은 알고리즘의 실행 시간의 상한과 하한을 모두 설명하는 큰 오메가 표기법과 큰 세타 표기법을 사용하는 것이다.

시간 복잡성 분석은 알고리즘과 데이터의 가정과 모델을 기반으로 하므로 실제로 결과를 검증하는 것이 중요합니다.

또한 알고리즘이 사용하는 메모리 또는 저장 공간의 양을 설명하는 공간 복잡성은 알고리즘의 효율성을 평가하는 데에도 사용될 수 있다.
```

# EP25 검색 알고리즘이 뭐죠?

```html
검색 알고리즘은 데이터 모음에서 특정 항목 또는 항목 그룹을 찾는 데 사용되는 기술 집합입니다. 검색 알고리즘의 일반적인 유형은 다음과 같다:

선형 검색: 이것은 첫 번째 항목부터 컬렉션의 각 요소를 순차적으로 확인하여 원하는 항목을 찾는 간단한 검색 알고리즘입니다. 시간 복잡도가 O(n)이므로 최악의 경우 항목을 검색하는 데 선형 시간이 소요됩니다.

이진 검색: 이 알고리즘은 정렬된 데이터 모음에서 항목을 검색하는 데 사용됩니다. 검색 간격을 반으로 나누고 원하는 항목이 간격의 중간 요소보다 작거나 크거나 같은지 확인하는 방식으로 작동합니다. 시간 복잡도가 O(log n)이므로 최악의 경우 항목을 검색하는 데 로그 시간이 걸립니다.
```

# 추가 공부, 또 다른 알고리즘은?

```html
깊이 우선 검색(DFS): 역추적 전에 각 분기를 따라 가능한 한 멀리 이동하여 그래프를 탐색하는 검색 알고리즘입니다. 이것은 O(V + E)의 시간 복잡도를 가지며, 여기서 V는 꼭짓점의 수이고 E는 그래프의 모서리의 수이다.

너비 우선 검색(BFS): 다음 수준으로 이동하기 전에 동일한 깊이 수준에서 모든 정점을 방문하여 그래프를 탐색하는 검색 알고리즘입니다. 이것은 O(V + E)의 시간 복잡도를 가지며, 여기서 V는 꼭짓점의 수이고 E는 그래프의 모서리의 수이다.

A* 검색: 이것은 그래프에서 두 점 사이의 최단 경로를 찾는 데 사용되는 검색 알고리즘입니다. 이것은 휴리스틱 함수와 시작 노드로부터의 거리의 조합을 사용하여 검색을 목표 노드로 안내한다. 그것은 O(b^d)의 시간 복잡성을 가지고 있는데, 여기서 b는 그래프의 분기 인자이고 d는 최적 솔루션의 깊이이다.

알고리즘의 선택은 응용 프로그램의 특정 문제와 제약 조건에 따라 달라지므로 서로 다른 알고리즘 간의 균형을 이해하고 프로젝트의 요구에 가장 적합한 알고리즘을 선택하는 것이 중요합니다.
```