# A* 알고리즘
주어진 출발점 부터 목표까지 가는 최단 경로를 찾아내는 그래프 탐색 알고리즘

현재 상태의 비용을 g(x), 현재 상태에서 다음 상태로 이동할 때의 휴리스틱 함수를 h(x)라고 할 때, **f(x)=g(x)+h(x)** 가 최소가 되는 지점을 우선적으로 탐색(휴리스틱 함수에 따라 성능이 갈린다)

휴리스틱 함수 : 가용한 정보를 기반으로 각 분기에서 어느 한 분기를 선택하기 위해 사용하는 함수

### 동작

1. f(x)를 오름차순 우선순위 큐에 노드로 삽입한다.
2. 우선순위 큐에서 최우선 노드를 pop한다.
3. 해당 노드에서 이동할 수 있는 노드를 찾는다.
4. 그 노드들의 f(x)를 구한다.
5. 그 노드들을 우선순위 큐에 삽입한다.
6. 목표 노드에 도달할 때까지 반복한다.


```python
//의사코드
PQ.push(start_node, g(start_node) + h(start_node))       //우선순위 큐에 시작 노드를 삽입한다.

while PQ is not empty       //우선순위 큐가 비어있지 않은 동안
    node = PQ.pop       //우선순위 큐를 pop한다.

    if node == goal_node       //만일 해당 노드가 목표 노드이면 반복문을 빠져나온다.
        break

    for next_node in (next_node_begin...next_node_end)       //해당 노드에서 이동할 수 있는 다음 노드들을 보는 동안
        PQ.push(next_node, g(node) + cost + h(next_node))       //우선순위 큐에 다음 노드를 삽입한다.

print goal_node_dist       //시작 노드에서 목표 노드까지의 거리를 출력한다.
```


---
### 출처
[나무위키 A* 알고리즘](https://namu.wiki/w/A*%20%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98#fn-%EC%B6%9C%EC%B2%98)