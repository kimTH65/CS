<h2> DFS , Depth-First Search</h2>

<div align="center">
<img height="400" src="https://github.com/kimTH65/cs/blob/main/dfs_bfs/Depth-First-Search.gif">
<h6>source : wikipedia(Depth-First-Search)</h6>
</div>

<br>
<h4>グラフの深さを優先して探索する方法、すべてのノードを訪問する必要があるときに使用)<br>
</h4>
<h6>
<a>　　</a>&nbsp(ノード訪問処理をすることが重要であり、ノード訪問の時に訪問可否を必ず検査する)
<br><br>
<a>　　</a>&nbsp(スタック、キュー、再帰関数を使用して実装可能)
</h6>  
<br>

```python

#Python
visited = [False for _ in range(n)] 

def dfs(graph,m,visited) :
    
    visited[m] = True # 訪問処理

    for g in graph[m]:
        if visited[g] == False : # 訪問しなかったNodeだけ訪問
            dfs(graph, m, visited)
            
```

<br>
<h2> BFS , Breadth-First Search</h2>
<div align="center">
<img height="400" src="https://github.com/kimTH65/cs/blob/main/dfs_bfs/Breadth-First-Search.gif">
<h6>source : wikipedia(Breadth-First-Search)</h6>
</div>

<br>
<h4>グラフを幅を優先して探索する方法、近くのノードを先に探索する方法(最短経路検索)
</h4>
<h6>
<a>　　</a>&nbsp(再帰を使わず、訪問処理/有無を検査することが重要)
&nbsp    
<br><br>
<a>　　</a>&nbsp(キューを使って実装可能)
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
<h5> - グラフのすべての頂点を訪問する場合、DFS、BFSの両方が使用可能
<br><br> - 経路の特徴があればDFS、最短距離はBFS
<br><br> - グラフがすごく大きいとDFS、適当ならBFSが有利
</h5>           
