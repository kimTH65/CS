<h2> DFS , 깊이 우선 탐색(Depth-First Search)</h2>

<div align="center">
<img height="400" src="https://github.com/kimTH65/cs/blob/main/dfs_bfs/Depth-First-Search.gif">
<h6>출처 : 위키피디아(Depth-First-Search)</h6>
</div>

<br>
<h4>그래프를 깊이를 우선으로 탐색하는 방법, 모든 노드를 방문해야 할 때 사용<br>
</h4>
<h6>
<a>　　</a>- 노드 방문처리 하는 것이 중요, 노드 방문 시 방문여부를 반드시 검사<br>
<br><br>
<a>　　</a>- 스택, 큐, 재귀함수를 사용하여 구현 가능<br>
</h6>  
<br>

```python

#Python
visited = [False for _ in range(n)] 

def dfs(graph,m,visited) :
    
    visited[m] = True # 방문 처리

    for g in graph[m]:
        if visited[g] == False : # 방문하지 않은 Node만 방문
            dfs(graph, m, visited)
            
```

<br>
<h2> BFS , 너비 우선 탐색(Breadth-First Search)</h2>
<div align="center">
<img height="400" src="https://github.com/kimTH65/cs/blob/main/dfs_bfs/Breadth-First-Search.gif">
<h6>출처 : 위키피디아(Breadth-First-Search)</h6>
</div>

<br>
<h4>그래프를 너비를 우선으로 탐색하는 방법, 가까운 노드를 먼저 탐색하는 방법(최단 경로 찾기)<br>
</h4>
<h6>
<a>　　</a>- 재귀를 사용하지 않고, 방문 처리/여부를 검사하는 것이 중요함<br>
&nbsp    
<br><br>
<a>　　</a>- 큐를 사용하여 구현 가능<br>
</h6>           
<br>

```python

#Python
from collections import deque

def bfs(graph, start):
    visit = list()
    que = deque()

    que.append(start)

    while que :
        node = que.pop(0)
        if node not in visit:
            visit.append(node)
            que.extend(graph[node])
    
```

<br>
<h2> DFS,BFS </h2>
<h5> - 그래프의 모든 정점을 방문하는 경우 DFS,BFS 둘 다 사용가능<br>
<br><br> - 경로의 특징이 있으면 DFS, 최단 거리는 BFS<br>
<br><br> - 그래프가 엄청 크면 DFS,적당하면 BFS가 유리함<br>
</h5>           
