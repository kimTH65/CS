# Sort
<h2>Bubble Sort</h2>
<br>
<div align="center">
<img src="https://github.com/kimTH65/cs/blob/main/sort/bubble.gif">
<h4>
接している二つの元素を比較して席を入れ替える
</h4>
</div>
<br>

```python

#Python
def bubble(arr):
    for i in range(len(arr)):
        for j in range(len(arr)-i-1):
            if(arr[j] > arr[j+1]):
                temp = arr[j]
                arr[j] = arr[j+1]
                arr[j+1] = temp

```

<br>
<br>


<h2>Selection Sort</h2>
<br>
<div align="center">
<img src="https://github.com/kimTH65/cs/blob/main/sort/selection.gif">
<h4>
該当値(Max/Min)を探して一番前と入れ替える
</h4>
</div>
<br>

```python

#Python
def selection(arr):
    for i in range(len(arr)):
        min_idx = i
        for j in range(i+1,len(arr)):
            if arr[min_idx] > arr[j]:
                min_idx = j
        arr[i],arr[min_idx] = arr[min_idx],arr[i]
        
```

<br>
<br>

<h2>Insertion Sort</h2>
<div align="center">
<br>
<img src="https://github.com/kimTH65/cs/blob/main/sort/insertion.gif">
<h4>
  移す値xを前の元素と比較して挿入位置を決め、挿入位置からxの前まで元素を後に移す
</h4>
</div>
<br>

```python

#Python
def insertion(arr):
    for i in range(1,len(arr)):
        for j in range(i,0,-1):
            if arr[j-1] > arr[j]:
                arr[j-1],arr[j] = arr[j],arr[j-1]

```

<br>
<br>    
<h2>Quick Sort</h2>
<br>
<div align="center">
<img src="https://github.com/kimTH65/cs/blob/main/sort/quick.gif">
<h4>
  中間値(Pivot)を求めてPivotより小さい値、大きい値で分ける -> 分けることがなければ終了
</h4>
</div>
<br>

```python

#Python
def quick(arr, start, end):
    if start >= end: 
        return arr

    pivot = start
    left = start +1
    right = end

    while(left <= right):

        while(left <= end and arr[left] <= arr[pivot]): #pivot 보다 큰값 찾으면 종료
            left += 1

        while(right > start and arr[right] >= arr[pivot]): # pivot 보다 작은 값 찾으면 종료
            right -= 1
        
        if(left > right): # 엇갈렸다면 작은 데이터와 pivot 교체
            arr[right], arr[pivot] = arr[pivot], arr[right]
        else: # 엇갈리지 않았다면 작은 데이터와 큰 데이터를 교체
            arr[left], arr[right] = arr[right], arr[left]
            
    # 분할하여 정렬 수행
    quick_sort(arr, start, right - 1)
    quick_sort(arr, right + 1, end)

```
                         
<br>
<br>

<h2>Merge Sort</h2>
<br>
<div align="center">
<img src="https://github.com/kimTH65/cs/blob/main/sort/merge.gif">
<h4>元素をすべて2で1個ずつに分割し、また2個ずつ合わせながら整列
</h4>
</div>
<br>

```python

#Python
def divide(list):
    if len(list) <= 1:
        return list
    mid = len(list) // 2
    leftList = list[:mid]
    rightList = list[mid:]
    leftList = divide(leftList)
    rightList = divide(rightList)
    return merge(leftList, rightList)

def merge(left, right):
    result = []
    while len(left) > 0 or len(right) > 0:
        if len(left) > 0 and len(right) > 0:
            if left[0] <= right[0]:
                result.append(left[0])
                left = left[1:]
            else:
                result.append(right[0])
                right = right[1:]
        elif len(left) > 0:
            result.append(left[0])
            left = left[1:]
        elif len(right) > 0:
            result.append(right[0])
            right = right[1:]
    return result

```

<br>
<br>

<h2>Heap Sort</h2>
<br>
<div align="center">
<img src="https://github.com/kimTH65/cs/blob/main/sort/heapy.gif">
<h4>
  優先順位Queue、完全バイナリツリー <br>
</h4>
</div>
<br>

```python

#Python
def heapify(arr, index, heap_size):
    largest = index
    left_index = 2 * index + 1
    right_index = 2 * index + 2
    if left_index < heap_size and arr[left_index] > arr[largest]:
        largest = left_index
    if right_index < heap_size and arr[right_index] > arr[largest]:
        largest = right_index
    if largest != index:
        arr[largest], arr[index] = arr[index], arr[largest]
        heapify(arr, largest, heap_size)

def heap_sort(arr):
    n = len(arr)
    for i in range(n // 2 - 1, -1, -1):
        heapify(arr, i, n)
    for i in range(n - 1, 0, -1):
        arr[0], arr[i] = arr[i], arr[0]
        heapify(arr, 0, i)
    return arr

```
