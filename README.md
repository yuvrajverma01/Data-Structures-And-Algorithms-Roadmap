# Data Structures And Algorithms Roadmap

### • [Practice Link](https://www.codingninjas.com/codestudio/guided-paths/data-structures-algorithms)

## • Arrays & Strings

- Basic Array & Strings Implementation
- Kadane's Algorithm (Max sum of continuous sub-array)
- Dutch National Flag Algorithm
- Sliding Window
- Two Pointers
- Traversal based problems
- Rotation Based Problems

## • Recursion & Backtracking

- Understanding Recursion
- Basic Recursion Questions
- Understanding Backtracking
- Divide & Conquer Algorithm

## • Sorting Algorithms

- Insertion Sort
- Binary Insertion Sort
- Selection Sort
- Bubble Sort
- Merge Sort
- Quick Sort
- Radix Sort

## • Binary Search Applications

- Binary Search Algorithm
- Binary Search On Arrays
- Binary Search On Matrix

## • Linked Lists

- Linked List Implementation
- Reversal Problems
- Sorting Linked Lists
- Slow and fast Pointers
- Modifying Linked Lists

## • Stacks (LIFO)

- Implementation
- Prefix, Postfix, Infix problems
- Applications/Problems

## • Queues (FIFO)

- Implementation
- Priority Queue
- Circular Queue
- Applications/Problems

## • Binary Trees

- Tree Traversals
- Construction Of Trees
- Tree Views
- Standard Problem

## • BST

- Construction Of BST
- Conversion Based Problems
- Modification in BST
- Standard Problems
- Priority Queues And Heaps
- Implementation Based problems
- Conversion based problems
- K Based Problems

## • Graphs

- Graph Traversals - BFS And DFS
- MST
- Shortest Path Algorithms
- Topological Sort
- Graphs in Matrix

## • Dynamic Programming

- DP with Arrays
- DP With Strings
- DP With Maths
- DP With Trees
- Breaking And Partition Based Problems
- Counting Based Problems
- Hard Recursion And Backtracking Questions

## • Other Topics

- Hashmaps
- Tries
- Bit Manipulation
- Greedy
- Circular Queues
- Deques - Hot Topic
- Doubly And Circular LL
- String Algorithms like KMP and Z 

#Algorithms

## Kadane's Algorithm

Time Complexity: **O(n)**
Algo's Objective: **Maximum Sum of Contiguous Subarray**
```
def kadanealgo(arr):
    maximum = min(arr)
    cur = 0
    for i in range(len(arr)):
        cur = cur + arr[i]
        if cur > maximum:
            maximum = cur
        if cur < 0:
            cur = 0
    return 
    
arr = [-2, -3, 4, -1, -2, 1, 5, -3]
print(kadanealgo(arr))

```

## Dutch National Flag Algorithm

Time Complexity: **O(n)**
Algo's Objective: **Sort an array of 0s, 1s and 2s**
```
def dutchflagalgo(arr):
    low = 0
    mid = 0
    high = len(arr) - 1
    while mid<=high:
        if arr[mid] == 0:   #Swap low with mid
            arr[low], arr[mid] = arr[mid], arr[low]
            low = low + 1
            mid = mid + 1
        elif arr[mid] == 1: #Increment the mid counter i.e. 1's
            mid = mid + 1
        else:   #Swap mid with high
            arr[mid], arr[high] = arr[high], arr[mid]
            high = high - 1
    return arr

     #low
arr = [0, 1, 1, 0, 1, 2, 1, 2, 0, 0, 0, 1]
     #mid                              #high
print(dutchflagalgo(arr))

```

## Algorithm

Time Complexity: **O()**
Algo's Objective: ****
```


```

## Algorithm

Time Complexity: **O()**
Algo's Objective: ****
```


```

## Algorithm

Time Complexity: **O()**
Algo's Objective: ****
```


```

## Algorithm

Time Complexity: **O()**
Algo's Objective: ****
```


```

## Algorithm

Time Complexity: **O()**
Algo's Objective: ****
```


```

## Algorithm

Time Complexity: **O()**
Algo's Objective: ****
```


```

