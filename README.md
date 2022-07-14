# *Python Cheat Sheet*

## Table of Contents
[Data Structures](#data-structures)
1. [list](#list)
1. [tuple](#tuple)
1. [set](#set)
1. [frozenset](#frozenset)
1. [str](#str)
1. [dict](#dict)
1. [numpy.ndarray](#numpy.ndarray)
1. [bytearray](#bytearray)

[Algorithms](#algorithms)
1. [DFS](#dfs)

[Techniques](#techniques)

## Data Structures
### list
- indexed collection of data
- inset/deleting at front requires shifting
``` python
a = [1,2]
a += [3]
a.index(2) # returns index of first instance of the value 2
a.remove(2) # removes first instance of the value 2
a.pop(1) # removes index (or last if not specified)
a.count(2) # counts number of 2s in the list
```
### tuple
- immutable list
``` python
a = (1,3,2)
b = (1,)
c = tuple(list1)
a[1]
```

### set
- uses hash table w/ linked list
``` python
a = set([2,1,3])
print(1 in set)
a.add(4)
```

### frozenset
- immutable set
``` python
a = frozenset([1,2,3])
```

### str
- immutable array of bytes (modifying creates a new string)
- represents unicode characters
``` python
a = "hel'
a[2]
a += "lo"
print("o" in a)
```

### dict
- collection of key-value pairs
- advanced version of hash table
``` python
a = {"a":2, "h":5}
a["b"] = 3
print("a" in a)
a["a"]
```

### numpy.ndarray
- uses numpy `import numpy as np`
```
a = np.array([2,3])
```

### bytearray
- sequence of integers
- integers are byte size: 0 <= x <= 255
``` python

```

## Algorithms
### DFS

``` python
def dfs(graph, visited, node):  #function for dfs 
    if node not in visited:
        print(node)
        visited.add(node)
        for neighbour in graph[node]:
            dfs(visited, graph, neighbour)
```
``` python
# Using a Python dictionary to act as an adjacency list
graph = {
  '5' : ['3','7'],
  '3' : ['2', '4'],
  '7' : ['8'],
  '2' : [],
  '4' : ['8'],
  '8' : []
}
visited = set() # Set to keep track of visited nodes of graph.
dfs(graph, visited, '5')
```

## Techniques