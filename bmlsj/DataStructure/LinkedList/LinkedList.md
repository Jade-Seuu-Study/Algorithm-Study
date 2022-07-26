# 연결 리스트(LinkedList)

각 노드가 데이터와 포인터를 가지고 한 줄로 연결되어 있는 방식으로 데이터를 저장하는 자료구조

데이터를 담고 있는 노드들이 연결되어 있는데, 노드의 포인터가 다음이나 이전의 노드와의 연결을 담당한다.
<br></br>
## 배열 vs 연결리스트

| | **배열** | **연결리스트**|
|--|--|--|
|**물리적 메모리 주소**| 연속적|  연속적이지 않고 랜덤|
|**삽입/삭제 시간**| O(n) | 동적이므로 O(1)|
|**접근 시간**| index를 이용해 O(1)만큼 소요 | 연결된 메모리가 아니기때문에 모든 노드를 거쳐서 탐색해야한다. O(n) 시간 소요 |
<br></br>
## 연결리스트 종류
1. **단일 연결 리스트(Singly LinkedList)**

    헤더 노드가 존재하며 헤더 노드는 다음 노드를 그리고 다음 노드는 그 다음 노드의 헤더는 그 다음 노드를 가리킨다. 한 방향으로 연결된 형태

    ![single](../../img/Single_linked_list.png)

2. **이중 연결 리스트(Doubly LinkedList)**

    헤더 노드만 존재하며, 각 노드는 다음 노드를 가리키는 링크를 가지는 동시에 이전 노드를 가리키는 링크를 가진다.

    ![double](../../img/Doubly_linked_list.png)

3. **원형 연결 리스트(Circular LinkedList)**

    헤더 노드와 테일 노드가 존재하며, 단순 연결 리스트와 구조상 동일하지만 테일 노드가 헤더 노드를 가리키고 있다는 것이 차이점이다.

    ![circular](../../img/Circurlar_linked_list.png)

<br></br>

## 파이썬에서의 포인터
C언어에서는 포인터를 사용해 다음 리스트를 가리키면 되지만 파이썬에서는 어떻게 가리켜야 할까?
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
```

노드를 위와 같이 구현하였다. 그럼 현재 노드에서 다음 노드를 어떻게 참조시킬 수 있을까?

```python
head = Node(5)          # 현재 노드의 위치
next_node = Node(12)    # next 노드의 위치
head.next = next_node   # 헤드가 다음 노드를 가리키게 함
```
5번 노드의 헤더가 12번 노드를 가리키고 있다.

<br></br>

<!--
## 1. 단일 연결 리스트(Singly LinkedList)
단순 연결 리스트에서 구현해야할 항목
- 첫 번째 노드 삽입
- 중간 노드 삽입
- 마지막 노드 삽입
- 노드 삭제 >
