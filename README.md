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

# Algorithms

## Kadane's Algorithm

#### Time Complexity: **O(n)**
#### Algo's Objective: **Maximum Sum of Contiguous Subarray**
```python

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

#### Time Complexity: **O(n)**
#### Algo's Objective: **Sort an array of 0s, 1s and 2s**
```python

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

## Sliding Window Algorithm

#### Time Complexity: **O(n)**
#### Algo's Objective: **Maximum/Minimum Sum of K size subarray**
```python

"""
1. windowsum: Store the sum of elements of current window
2. maximum: Store the maximum sum while iterating through windows
3. While running the for loop, we are removing the 1st element of the current window and adding the rightmost element (not included) of the window.

"""

def slidingwindow(arr, k):
    windowsum = sum(arr[:k])
    maximum = windowsum
    n = len(arr)

    for i in range(n-k):
        windowsum = windowsum - arr[i] + arr[i+k]
        maximum = max(windowsum, maximum)
    return maximum
    
arr = [1, 4, 2, 10, 2, 3, 1, 0, 20]
k = 3
print(slidingwindow(arr, k))

```

#### Time Complexity: **O(n²)**
#### Algo's Objective: **Smallest subarray with given Sum**
```python

def slidingwindow(arr, target):
    windowsum = 0              #Current window sum
    j = 0                      #Window Start
    jsize = max(arr)           #Current Window Size

    for i in range(len(arr)):
        windowsum = windowsum + arr[i]

        while windowsum >= target:
            jsize = min(jsize, i - j + 1)
            windowsum = windowsum - arr[j]
            j = j + 1
    return jsize

    
arr = [4, 2, 2, 7, 8, 1, 2, 8, 1, 0]
target = 8
print(slidingwindow(arr, target))

```

##  Algorithm

#### Time Complexity: **O()**
#### Algo's Objective: ****
```python



```

##  Algorithm

#### Time Complexity: **O()**
#### Algo's Objective: ****
```python



```

##  Algorithm

#### Time Complexity: **O()**
#### Algo's Objective: ****
```python



```

##  Algorithm

#### Time Complexity: **O()**
#### Algo's Objective: ****
```python



```

##  Algorithm

#### Time Complexity: **O()**
#### Algo's Objective: ****
```python



```

##  Algorithm

#### Time Complexity: **O()**
#### Algo's Objective: ****
```python



```


