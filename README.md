# We'll be adding new stuff here in Nov, 2022

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

## Two Pointer Algorithm

#### Time Complexity: **O(n)**

#### Algo's Objective: **Find pairs in an array with a sum equal to k**

```python

def twopointeralgo(arr, k):
    i = 0              #represents first pointer
    j = len(arr) - 1   #represents second pointer
 
    while i<j:
        if (arr[i] + arr[j] == k):   #If we find a pair
            return 1
        elif(arr[i] + arr[j] < k):
            i = i + 1
        else:
            j -= 1
    return 0
 
arr = [3, 5, 9, 2, 8, 10, 11]
k = 17
print(twopointeralgo(arr, k))

```

## Three Pointer Algorithm

#### Time Complexity: **O(n)**

#### Algo's Objective: **Find triplets in an array with a sum equal to k**

```python



```

## 

#### Time Complexity: **O()**

#### Algo's Objective: ****

```python



```

# Questions/Practice

## • Arrays

- [Reverse the array.](https://www.geeksforgeeks.org/write-a-program-to-reverse-an-array-or-string/)
- [Maximum and Minimum in an array.](https://www.geeksforgeeks.org/maximum-and-minimum-in-an-array/)
- [K<sup>th</sup> Max and Min in an array.](https://practice.geeksforgeeks.org/problems/kth-smallest-element/0)
- [Sort an array which consists of only 0s, 1s and 2s.](https://practice.geeksforgeeks.org/problems/sort-an-array-of-0s-1s-and-2s/0)
- [Move all negative elements to one side of the array.](https://www.geeksforgeeks.org/move-negative-numbers-beginning-positive-end-constant-extra-space/)
- [Find Union and Intersection of two sorted arrays.](https://practice.geeksforgeeks.org/problems/union-of-two-arrays/0)
- [Rotate an array cyclically by one.](https://practice.geeksforgeeks.org/problems/cyclically-rotate-an-array-by-one/0)
- [Find largest sum of a contiguous subarray.](https://practice.geeksforgeeks.org/problems/kadanes-algorithm/0)
- [Minimize the maximum difference between heights.](https://practice.geeksforgeeks.org/problems/minimize-the-heights3351/1)
- [Minimum number of jumps to reach an end of an array.](https://practice.geeksforgeeks.org/problems/minimum-number-of-jumps/0)
- [Find duplicates in an array of N+1 integers.](https://leetcode.com/problems/find-the-duplicate-number/)
- [Merge two sorted arrays without using extra space.](https://practice.geeksforgeeks.org/problems/merge-two-sorted-arrays5135/1)
- [Solve Kadane's Algorithm.](https://practice.geeksforgeeks.org/problems/kadanes-algorithm/0)
- [Count Inversion.](https://practice.geeksforgeeks.org/problems/inversion-of-array/0)
- [Best time to buy or sell stock.](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- [Find pair of elements whose sum is equal to K.](https://practice.geeksforgeeks.org/problems/count-pairs-with-given-sum5022/1)
- [Find common elements in 3 sorted arrays.](https://practice.geeksforgeeks.org/problems/common-elements1132/1)
- [Find if there is any subarray with sum equal to 0.](https://practice.geeksforgeeks.org/problems/subarray-with-0-sum/0)
- [Find factorial of a large number.](https://practice.geeksforgeeks.org/problems/factorials-of-large-numbers/0)
- [Find maximum product subarray.](https://practice.geeksforgeeks.org/problems/maximum-product-subarray3604/1)
- [Find longest consecutive subsequence.](https://practice.geeksforgeeks.org/problems/longest-consecutive-subsequence/0)
- [Given an array of size n and a number k, find all elements that appear more than "N/K" times.](https://www.geeksforgeeks.org/given-an-array-of-of-size-n-finds-all-the-elements-that-appear-more-than-nk-times/)
- [Max profit by buying and selling a share atmost twice.](https://www.geeksforgeeks.org/maximum-profit-by-buying-and-selling-a-share-at-most-twice/)
- [Find whether an array is subset of another array.](https://practice.geeksforgeeks.org/problems/array-subset-of-another-array/0)
- [Find the Triplet that sum to a given value.](https://practice.geeksforgeeks.org/problems/triplet-sum-in-array/0)
- [Trapping rain water problem.](https://practice.geeksforgeeks.org/problems/trapping-rain-water/0)
- [Chocolate Distribution problem.](https://practice.geeksforgeeks.org/problems/chocolate-distribution-problem/0)
- [Smallest subarray with sum greater than K.](https://practice.geeksforgeeks.org/problems/smallest-subarray-with-sum-greater-than-x/0)
- [Three way partitioning of an array around a given value.](https://practice.geeksforgeeks.org/problems/three-way-partitioning/1)
- [Min swaps required bring elements less equal to K together.](https://practice.geeksforgeeks.org/problems/minimum-swaps-required-to-bring-all-elements-less-than-or-equal-to-k-together/0)
- [Min no. of operations required to make an array palindrome.](https://practice.geeksforgeeks.org/problems/palindromic-array/0)
- [Median of 2 sorted 2 arrays of equal size.](https://practice.geeksforgeeks.org/problems/find-the-median0527/1)
- [Median of 2 sorted arrays of different size.](https://www.geeksforgeeks.org/median-of-two-sorted-arrays-of-different-sizes/)

## • Arrays [MATRIX Problems]

- [Spiral traversal on a Matrix.](https://practice.geeksforgeeks.org/problems/spirally-traversing-a-matrix/0)
- [Search an element in a matriix.](https://leetcode.com/problems/search-a-2d-matrix/)
- [Find median in a row wise sorted matrix.](https://practice.geeksforgeeks.org/problems/median-in-a-row-wise-sorted-matrix1527/1)
- [Find row with maximum no. of 1's.](https://practice.geeksforgeeks.org/problems/row-with-max-1s0023/1)
- [Print elements in sorted order using row-column wise sorted matrix.](https://practice.geeksforgeeks.org/problems/sorted-matrix/0)
- [Maximum size rectangle.](https://practice.geeksforgeeks.org/problems/max-rectangle/1)
- [Find a specific pair in matrix.](https://www.geeksforgeeks.org/find-a-specific-pair-in-matrix/)
- [Rotate matrix by 90 degrees.](https://www.geeksforgeeks.org/rotate-a-matrix-by-90-degree-in-clockwise-direction-without-using-any-extra-space/)
- [Kth smallest element in a row-column wise sorted matrix.](https://practice.geeksforgeeks.org/problems/kth-element-in-matrix/1)
- [Common elements in all rows of a given matrix.](https://www.geeksforgeeks.org/common-elements-in-all-rows-of-a-given-matrix/)

## • String

- [Reverse a String.](https://leetcode.com/problems/reverse-string/)
- [Check whether a String is Palindrome or not.](https://practice.geeksforgeeks.org/problems/palindrome-string0817/1)
- [Find Duplicate characters in a string.](https://www.geeksforgeeks.org/print-all-the-duplicates-in-the-input-string/)
- [Write a Code to check whether one string is a rotation of another.](https://www.geeksforgeeks.org/a-program-to-check-if-strings-are-rotations-of-each-other/)
- [Write a Program to check whether a string is a valid shuffle of two strings or not.](https://www.programiz.com/java-programming/examples/check-valid-shuffle-of-strings)
- [Count and Say problem.](https://leetcode.com/problems/count-and-say/)
- [Write a program to find the longest Palindrome in a string.\* Longest palindromic Substring](https://practice.geeksforgeeks.org/problems/longest-palindrome-in-a-string/0)
- [Find Longest Recurring Subsequence in String.](https://practice.geeksforgeeks.org/problems/longest-repeating-subsequence/0)
- [Print all Subsequences of a string.](https://www.geeksforgeeks.org/print-subsequences-string/)
- [Print all the permutations of the given string.](https://practice.geeksforgeeks.org/problems/permutations-of-a-given-string/0)
- [Split the Binary string into two substring with equal 0’s and 1’s.](https://www.geeksforgeeks.org/split-the-binary-string-into-substrings-with-equal-number-of-0s-and-1s/)
- [Word Wrap Problem.](https://practice.geeksforgeeks.org/problems/word-wrap/0)
- [EDIT Distance.](https://practice.geeksforgeeks.org/problems/edit-distance3702/1)
- [Find next greater number with same set of digits.](https://practice.geeksforgeeks.org/problems/next-permutation/0)
- [Balanced Parenthesis problem.](https://practice.geeksforgeeks.org/problems/parenthesis-checker/0)
- [Word break Problem.](https://practice.geeksforgeeks.org/problems/word-break/0)
- [Rabin Karp Algo.](https://www.geeksforgeeks.org/rabin-karp-algorithm-for-pattern-searching/)
- [KMP Algo.](https://practice.geeksforgeeks.org/problems/longest-prefix-suffix2527/1)
- [Convert a Sentence into its equivalent mobile numeric keypad sequence.](https://www.geeksforgeeks.org/convert-sentence-equivalent-mobile-numeric-keypad-sequence/)
- [Minimum number of bracket reversals needed to make an expression balanced.](https://practice.geeksforgeeks.org/problems/count-the-reversals/0)
- [Count All Palindromic Subsequence in a given String.](https://practice.geeksforgeeks.org/problems/count-palindromic-subsequences/1)
- [Count of number of given string in 2D character array.](https://www.geeksforgeeks.org/find-count-number-given-string-present-2d-character-array/)
- [Search a Word in a 2D Grid of characters.](https://practice.geeksforgeeks.org/problems/find-the-string-in-grid/0)
- [Boyer Moore Algorithm for Pattern Searching.](https://www.geeksforgeeks.org/boyer-moore-algorithm-for-pattern-searching/)
- [Converting Roman Numerals to Decimal.](https://practice.geeksforgeeks.org/problems/roman-number-to-integer/0)
- [Longest Common Prefix.](https://leetcode.com/problems/longest-common-prefix/)
- [Number of flips to make binary string alternate.](https://practice.geeksforgeeks.org/problems/min-number-of-flips/0)
- [Find the first repeated word in string.](https://practice.geeksforgeeks.org/problems/second-most-repeated-string-in-a-sequence/0)
- [Minimum number of swaps for bracket balancing.](https://practice.geeksforgeeks.org/problems/minimum-swaps-for-bracket-balancing/0)
- [Find the longest common subsequence between two strings.](https://practice.geeksforgeeks.org/problems/longest-common-subsequence/0)
- [Program to generate all possible valid IP addresses from given string.](https://www.geeksforgeeks.org/program-generate-possible-valid-ip-addresses-given-string/)
- [Write a program tofind the smallest window that contains all characters of string itself.](https://practice.geeksforgeeks.org/problems/smallest-distant-window/0)
- [Rearrange characters in a string such that no two adjacent are same.](https://practice.geeksforgeeks.org/problems/rearrange-characters/0)
- [Minimum characters to be added at front to make string palindrome.](https://www.geeksforgeeks.org/minimum-characters-added-front-make-string-palindrome/)
- [Given a sequence of words, print all anagrams together.](https://practice.geeksforgeeks.org/problems/k-anagrams-1/0)
- [Find the smallest window in a string containing all characters of another string.](https://practice.geeksforgeeks.org/problems/smallest-window-in-a-string-containing-all-the-characters-of-another-string/0)
- [Recursively remove all adjacent duplicates.](https://practice.geeksforgeeks.org/problems/consecutive-elements/0)
- [String matching where one string contains wildcard characters.](https://practice.geeksforgeeks.org/problems/wildcard-string-matching/0)
- [Function to find Number of customers who could not get a computer.](https://www.geeksforgeeks.org/function-to-find-number-of-customers-who-could-not-get-a-computer/)
- [Transform One String to Another using Minimum Number of Given Operation.](https://www.geeksforgeeks.org/transform-one-string-to-another-using-minimum-number-of-given-operation/)
- [Check if two given strings are isomorphic to each other.](https://practice.geeksforgeeks.org/problems/isomorphic-strings/0)
- [Recursively print all sentences that can be formed from list of word lists.](https://www.geeksforgeeks.org/recursively-print-all-sentences-that-can-be-formed-from-list-of-word-lists/)

## • Searching and Sorting

- [Find first and last positions of an element in a sorted array.](https://practice.geeksforgeeks.org/problems/first-and-last-occurrences-of-x/0)
- [Find a Fixed Point (Value equal to index) in a given array.](https://practice.geeksforgeeks.org/problems/value-equal-to-index-value1330/1)
- [Search in a rotated sorted array.](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- [Square root of an integer.](https://practice.geeksforgeeks.org/problems/count-squares3649/1)
- [Maximum and minimum of an array using minimum number of comparisons.](https://practice.geeksforgeeks.org/problems/middle-of-three2926/1)
- [Optimum location of point to minimize total distance.](https://www.geeksforgeeks.org/optimum-location-point-minimize-total-distance/#:~:text=We%20need%20to%20find%20a,set%20of%20points%20is%20minimum.&text=In%20above%20figure%20optimum%20location,is%20minimum%20obtainable%20total%20distance.)
- [Find the repeating and the missing.](https://practice.geeksforgeeks.org/problems/find-missing-and-repeating2512/1)
- [Find majority element.](https://practice.geeksforgeeks.org/problems/majority-element/0)
- [Searching in an array where adjacent differ by at most k.](https://www.geeksforgeeks.org/searching-array-adjacent-differ-k/)
- [Find a pair with a given difference.](https://practice.geeksforgeeks.org/problems/find-pair-given-difference/0)
- [Find four elements that sum to a given value.](https://practice.geeksforgeeks.org/problems/find-all-four-sum-numbers/0)
- [Maximum sum such that no 2 elements are adjacent.](https://practice.geeksforgeeks.org/problems/stickler-theif/0)
- [Count triplet with sum smaller than a given value.](https://practice.geeksforgeeks.org/problems/count-triplets-with-sum-smaller-than-x5549/1)
- [Merge 2 sorted arrays.](https://practice.geeksforgeeks.org/problems/merge-two-sorted-arrays5135/1)
- [Print all subarrays with 0 sum.](https://practice.geeksforgeeks.org/problems/zero-sum-subarrays/0)
- [Product array Puzzle.](https://practice.geeksforgeeks.org/problems/product-array-puzzle/0)
- [Sort array according to count of set bits.](https://practice.geeksforgeeks.org/problems/sort-by-set-bit-count/0)
- [Minimum no. of swaps required to sort the array.](https://practice.geeksforgeeks.org/problems/minimum-swaps/1)
- [Bishu and Soldiers.](https://www.hackerearth.com/practice/algorithms/searching/binary-search/practice-problems/algorithm/bishu-and-soldiers/)
- [Rasta and Kheshtak.](https://www.hackerearth.com/practice/algorithms/searching/binary-search/practice-problems/algorithm/rasta-and-kheshtak/)
- [Kth smallest number again.](https://www.hackerearth.com/practice/algorithms/searching/binary-search/practice-problems/algorithm/kth-smallest-number-again-2/)
- [Find pivot element in a sorted array.](http://theoryofprogramming.com/2017/12/16/find-pivot-element-sorted-rotated-array/)
- [K-th Element of Two Sorted Arrays.](https://practice.geeksforgeeks.org/problems/k-th-element-of-two-sorted-array/0)
- [Book Allocation Problem.](https://practice.geeksforgeeks.org/problems/allocate-minimum-number-of-pages/0)
- [Job Scheduling Algo.](https://www.geeksforgeeks.org/weighted-job-scheduling-log-n-time/)
- [Missing Number in AP.](https://practice.geeksforgeeks.org/problems/arithmetic-number/0)
- [Smallest number with atleastn trailing zeroes infactorial.](https://practice.geeksforgeeks.org/problems/smallest-factorial-number5929/1)
- [Painters Partition Problem:](https://www.geeksforgeeks.org/painters-partition-problem/)
- [ROTI-Prata SPOJ.](https://www.spoj.com/problems/PRATA/)
- [DoubleHelix SPOJ.](https://www.spoj.com/problems/ANARC05B/)
- [Subset Sums.](https://www.spoj.com/problems/SUBSUMS/)
- [Find the inversion count.](https://practice.geeksforgeeks.org/problems/inversion-of-array/0)
- [Implement Merge-sort in-place.](https://www.geeksforgeeks.org/in-place-merge-sort/)
- [Partitioning and Sorting Arrays with Many Repeated Entries.](https://www.baeldung.com/java-sorting-arrays-with-repeated-entries)

## • Linked List

- [Write a Program to reverse the Linked List.](https://www.geeksforgeeks.org/reverse-a-linked-list/)
- [Reverse a Linked List in group of Given Size.](https://practice.geeksforgeeks.org/problems/reverse-a-linked-list-in-groups-of-given-size/1)
- [Write a program to Detect loop in a linked list.](https://practice.geeksforgeeks.org/problems/detect-loop-in-linked-list/1)
- [Write a program to Delete loop in a linked list.](https://practice.geeksforgeeks.org/problems/remove-loop-in-linked-list/1)
- [Find the starting point of the loop. ](https://www.geeksforgeeks.org/find-first-node-of-loop-in-a-linked-list/)
- [Remove Duplicates in a sorted Linked List.](https://practice.geeksforgeeks.org/problems/remove-duplicate-element-from-sorted-linked-list/1)
- [Remove Duplicates in a Un-sorted Linked List.](https://practice.geeksforgeeks.org/problems/remove-duplicates-from-an-unsorted-linked-list/1)
- [Write a Program to Move the last element to Front in a Linked List.](https://www.geeksforgeeks.org/move-last-element-to-front-of-a-given-linked-list/)
- [Add “1” to a number represented as a Linked List.](https://practice.geeksforgeeks.org/problems/add-1-to-a-number-represented-as-linked-list/1)
- [Add two numbers represented by linked lists.](https://practice.geeksforgeeks.org/problems/add-two-numbers-represented-by-linked-lists/1)
- [Intersection of two Sorted Linked List.](https://practice.geeksforgeeks.org/problems/intersection-of-two-sorted-linked-lists/1)
- [Intersection Point of two Linked Lists](https://practice.geeksforgeeks.org/problems/intersection-point-in-y-shapped-linked-lists/1).
- [Merge Sort For Linked lists.](https://practice.geeksforgeeks.org/problems/sort-a-linked-list/1)
- [Quicksort for Linked Lists.](https://practice.geeksforgeeks.org/problems/quick-sort-on-linked-list/1)
- [Find the middle Element of a linked list.](https://leetcode.com/problems/middle-of-the-linked-list/)
- [Check if a linked list is a circular linked list.](https://practice.geeksforgeeks.org/problems/circular-linked-list/1)
- [Split a Circular linked list into two halves.](https://practice.geeksforgeeks.org/problems/split-a-circular-linked-list-into-two-halves/1)
- [Write a Program to check whether the Singly Linked list is a palindrome or not.](https://practice.geeksforgeeks.org/problems/check-if-linked-list-is-pallindrome/1)
- [Deletion from a Circular Linked List.](https://www.geeksforgeeks.org/deletion-circular-linked-list/)
- [Reverse a Doubly Linked list.](https://practice.geeksforgeeks.org/problems/reverse-a-doubly-linked-list/1)
- [Find pairs with a given sum in a DLL.](https://www.geeksforgeeks.org/find-pairs-given-sum-doubly-linked-list/)
- [Count triplets in a sorted DLL whose sum is equal to given value “X”.](https://www.geeksforgeeks.org/count-triplets-sorted-doubly-linked-list-whose-sum-equal-given-value-x/)
- [Sort a “k” sorted Doubly Linked list.](https://www.geeksforgeeks.org/sort-k-sorted-doubly-linked-list/)
- [Rotate DoublyLinked list by N nodes.](https://www.geeksforgeeks.org/rotate-doubly-linked-list-n-nodes/)
- [Rotate a Doubly Linked list in group of Given Size.](https://www.geeksforgeeks.org/reverse-doubly-linked-list-groups-given-size/)
- Can we reverse a linked list in less than O(n)?
- Why Quicksort is preferred for. Arrays and Merge Sort for Linked Lists?
- [Flatten a Linked List.](https://practice.geeksforgeeks.org/problems/flattening-a-linked-list/1)
- [Sort a LL of 0's, 1's and 2's.](https://practice.geeksforgeeks.org/problems/given-a-linked-list-of-0s-1s-and-2s-sort-it/1)
- [Clone a linked list with next and random pointer.](https://practice.geeksforgeeks.org/problems/clone-a-linked-list-with-next-and-random-pointer/1)
- [Merge K sorted Linked list.](https://practice.geeksforgeeks.org/problems/merge-k-sorted-linked-lists/1)
- [Multiply 2 no. represented by LL.](https://practice.geeksforgeeks.org/problems/multiply-two-linked-lists/1)
- [Delete nodes which have a greater value on right side.](https://practice.geeksforgeeks.org/problems/delete-nodes-having-greater-value-on-right/1)
- [Segregate even and odd nodes in a Linked List.](https://practice.geeksforgeeks.org/problems/segregate-even-and-odd-nodes-in-a-linked-list/0)
- [Program for n’th node from the end of a Linked List.](https://practice.geeksforgeeks.org/problems/nth-node-from-end-of-linked-list/1)
- [Find the first non-repeating character from a stream of characters.](https://practice.geeksforgeeks.org/problems/first-non-repeating-character-in-a-stream/0)

## • Binary Trees

- [Level order traversal.](https://practice.geeksforgeeks.org/problems/level-order-traversal/1)
- [Reverse Level Order traversal.](https://practice.geeksforgeeks.org/problems/reverse-level-order-traversal/1)
- [Height of a tree.](https://practice.geeksforgeeks.org/problems/height-of-binary-tree/1)
- [Diameter of a tree.](https://practice.geeksforgeeks.org/problems/diameter-of-binary-tree/1)
- [Mirror of a tree.](https://www.geeksforgeeks.org/create-a-mirror-tree-from-the-given-binary-tree/)
- [Inorder Traversal of a tree both using recursion and Iteration](https://www.techiedelight.com/inorder-tree-traversal-iterative-recursive/).
- [Preorder Traversal of a tree both using recursion and Iteration.](https://www.techiedelight.com/preorder-tree-traversal-iterative-recursive/)
- [Postorder Traversal of a tree both using recursion and Iteration.](https://www.techiedelight.com/postorder-tree-traversal-iterative-recursive/)
- [Left View of a tree.](https://practice.geeksforgeeks.org/problems/left-view-of-binary-tree/1)
- [Right View of Tree.](https://practice.geeksforgeeks.org/problems/right-view-of-binary-tree/1)
- [Top View of a tree.](https://practice.geeksforgeeks.org/problems/top-view-of-binary-tree/1)
- [Bottom View of a tree.](https://practice.geeksforgeeks.org/problems/bottom-view-of-binary-tree/1)
- [Zig-Zag traversal of a binary tree.](https://practice.geeksforgeeks.org/problems/zigzag-tree-traversal/1)
- [Check if a tree is balanced or not.](https://practice.geeksforgeeks.org/problems/check-for-balanced-tree/1)
- [Diagnol Traversal of a Binary tree.](https://www.geeksforgeeks.org/diagonal-traversal-of-binary-tree/)
- [Boundary traversal of a Binary tree.](https://practice.geeksforgeeks.org/problems/boundary-traversal-of-binary-tree/1)
- [Construct Binary Tree from String with Bracket Representation.](https://www.geeksforgeeks.org/construct-binary-tree-string-bracket-representation/)
- [Convert Binary tree into Doubly Linked List.](https://practice.geeksforgeeks.org/problems/binary-tree-to-dll/1)
- [Convert Binary tree into Sum tree.](https://practice.geeksforgeeks.org/problems/transform-to-sum-tree/1)
- [Construct Binary tree from Inorder and preorder traversal.](https://practice.geeksforgeeks.org/problems/construct-tree-1/1)
- [Find minimum swaps required to convert a Binary tree into BST.](https://www.geeksforgeeks.org/minimum-swap-required-convert-binary-tree-binary-search-tree/#:~:text=Given%20the%20array%20representation%20of,it%20into%20Binary%20Search%20Tree.&text=Swap%201%3A%20Swap%20node%208,node%209%20with%20node%2010.)
- [Check if Binary tree is Sum tree or not.](https://practice.geeksforgeeks.org/problems/sum-tree/1)
- [Check if all leaf nodes are at same level or not.](https://practice.geeksforgeeks.org/problems/leaf-at-same-level/1)
- [Check if a Binary Tree contains duplicate subtrees of size 2 or more.](https://practice.geeksforgeeks.org/problems/duplicate-subtree-in-binary-tree/1)
- [Check if 2 trees are mirror or not.](https://practice.geeksforgeeks.org/problems/check-mirror-in-n-ary-tree/0)
- [Sum of Nodes on the Longest path from root to leaf node.](https://practice.geeksforgeeks.org/problems/sum-of-the-longest-bloodline-of-a-tree/1)
- [Check if given graph is tree or not.](https://www.geeksforgeeks.org/check-given-graph-tree/#:~:text=Since%20the%20graph%20is%20undirected,graph%20is%20connected%2C%20otherwise%20not.)
- [Find Largest subtree sum in a tree.](https://www.geeksforgeeks.org/find-largest-subtree-sum-tree/)
- [Maximum Sum of nodes in Binary tree such that no two are adjacent.](https://www.geeksforgeeks.org/maximum-sum-nodes-binary-tree-no-two-adjacent/)
- [Print all "K" Sum paths in a Binary tree.](https://www.geeksforgeeks.org/print-k-sum-paths-binary-tree/)
- [Find LCA in a Binary tree.](https://practice.geeksforgeeks.org/problems/lowest-common-ancestor-in-a-binary-tree/1)
- [Find distance between 2 nodes in a Binary tree.](https://practice.geeksforgeeks.org/problems/min-distance-between-two-given-nodes-of-a-binary-tree/1)
- [Kth Ancestor of node in a Binary tree.](https://www.geeksforgeeks.org/kth-ancestor-node-binary-tree-set-2/)
- [Find all Duplicate subtrees in a Binary tree.](https://practice.geeksforgeeks.org/problems/duplicate-subtrees/1)
- [Tree Isomorphism Problem.](https://practice.geeksforgeeks.org/problems/check-if-tree-is-isomorphic/1)

## • Binary Search Trees

- [Find a value in a BST.](https://www.geeksforgeeks.org/binary-search-tree-set-1-search-and-insertion/)
- [Deletion of a node in a BST.](https://leetcode.com/problems/delete-node-in-a-bst/)
- [Find min and max value in a BST.](https://practice.geeksforgeeks.org/problems/minimum-element-in-bst/1)
- [Find inorder successor and inorder predecessor in a BST.](https://practice.geeksforgeeks.org/problems/predecessor-and-successor/1)
- [Check if a tree is a BST or not.](https://practice.geeksforgeeks.org/problems/check-for-bst/1)
- [Populate Inorder successor of all nodes.](https://practice.geeksforgeeks.org/problems/populate-inorder-successor-for-all-nodes/1)
- [Find LCA of 2 nodes in a BST.](https://practice.geeksforgeeks.org/problems/lowest-common-ancestor-in-a-bst/1)
- [Construct BST from preorder traversal.](https://www.geeksforgeeks.org/construct-bst-from-given-preorder-traversa/)
- [Convert Binary tree into BST.](https://practice.geeksforgeeks.org/problems/binary-tree-to-bst/1)
- [Convert a normal BST into a Balanced BST.](https://www.geeksforgeeks.org/convert-normal-bst-balanced-bst/)
- [Merge two BST.](https://www.geeksforgeeks.org/merge-two-balanced-binary-search-trees/)
- [Find Kth largest element in a BST.](https://practice.geeksforgeeks.org/problems/kth-largest-element-in-bst/1)
- [Find Kth smallest element in a BST.](https://practice.geeksforgeeks.org/problems/find-k-th-smallest-element-in-bst/1)
- [Count pairs from 2 BST whose sum is equal to given value "X".](https://practice.geeksforgeeks.org/problems/brothers-from-different-root/1)
- [Find the median of BST in O(n) time and O(1) space.](https://www.geeksforgeeks.org/find-median-bst-time-o1-space/)
- [Count BST ndoes that lie in a given range.](https://practice.geeksforgeeks.org/problems/count-bst-nodes-that-lie-in-a-given-range/1)
- [Replace every element with the least greater element on its right.](https://www.geeksforgeeks.org/replace-every-element-with-the-least-greater-element-on-its-right/)
- [Given "n" appointments, find the conflicting appointments.](https://www.geeksforgeeks.org/given-n-appointments-find-conflicting-appointments/)
- [Check preorder is valid or not.](https://practice.geeksforgeeks.org/problems/preorder-to-postorder/0)
- [Check whether BST contains Dead end.](https://practice.geeksforgeeks.org/problems/check-whether-bst-contains-dead-end/1)
- [Largest BST in a Binary Tree.](https://practice.geeksforgeeks.org/problems/largest-bst/1)
- [Flatten BST to sorted list.](https://www.geeksforgeeks.org/flatten-bst-to-sorted-list-increasing-order/)

## • Greedy

- [Activity Selection Problem.](https://practice.geeksforgeeks.org/problems/n-meetings-in-one-room/0)
- [Job Sequencing Problem.](https://practice.geeksforgeeks.org/problems/job-sequencing-problem/0)
- [Huffman Coding.](https://practice.geeksforgeeks.org/problems/huffman-encoding/0)
- [Water Connection Problem.](https://practice.geeksforgeeks.org/problems/water-connection-problem/0)
- [Fractional Knapsack Problem.](https://practice.geeksforgeeks.org/problems/fractional-knapsack/0)
- [Greedy Algorithm to find Minimum number of Coins.](https://practice.geeksforgeeks.org/problems/coin-piles/0)
- [Maximum trains for which stoppage can be provided.](https://www.geeksforgeeks.org/maximum-trains-stoppage-can-provided/)
- [Minimum Platforms Problem.](https://practice.geeksforgeeks.org/problems/minimum-platforms/0)
- [Buy Maximum Stocks if i stocks can be bought on i-th day.](https://www.geeksforgeeks.org/buy-maximum-stocks-stocks-can-bought-th-day/)
- [Find the minimum and maximum amount to buy all N candies.](https://practice.geeksforgeeks.org/problems/shop-in-candy-store/0)
- [Minimize Cash Flow among a given set of friends who have borrowed money from each other.](https://www.geeksforgeeks.org/minimize-cash-flow-among-given-set-friends-borrowed-money/)
- [Minimum Cost to cut a board into squares.](https://www.geeksforgeeks.org/minimum-cost-cut-board-squares/)
- [Check if it is possible to survive on Island.](https://www.geeksforgeeks.org/survival/)
- [Find maximum meetings in one room.](https://www.geeksforgeeks.org/find-maximum-meetings-in-one-room/)
- [Maximum product subset of an array.](https://www.geeksforgeeks.org/maximum-product-subset-array/)
- [Maximize array sum after K negations.](https://practice.geeksforgeeks.org/problems/maximize-sum-after-k-negations/0)
- [Maximize the sum of arri\*i.](https://practice.geeksforgeeks.org/problems/maximize-arrii-of-an-array/0)
- [Maximum sum of absolute difference of an array.](https://www.geeksforgeeks.org/maximum-sum-absolute-difference-array/)
- [Maximize sum of consecutive differences in a circular array](https://practice.geeksforgeeks.org/problems/swap-and-maximize/0)
- [Minimum sum of absolute difference of pairs of two arrays.](https://www.geeksforgeeks.org/minimum-sum-absolute-difference-pairs-two-arrays/#:~:text=It%20consists%20of%20two%20steps,result%20to%20the%20sum%20S.)
- [Program for Shortest Job First (or SJF) CPU Scheduling.](https://www.geeksforgeeks.org/program-for-shortest-job-first-or-sjf-cpu-scheduling-set-1-non-preemptive/)
- [Program for Least Recently Used (LRU) Page Replacement algorithm.](https://practice.geeksforgeeks.org/problems/page-faults-in-lru/0)
- [Smallest subset with sum greater than all other elements.](https://www.geeksforgeeks.org/smallest-subset-sum-greater-elements/)
- [Chocolate Distribution Problem.](https://practice.geeksforgeeks.org/problems/chocolate-distribution-problem/0)
- [DEFKIN - Defense of a Kingdom.](https://www.spoj.com/problems/DEFKIN/)
- [DIEHARD - DIE HARD.](https://www.spoj.com/problems/DIEHARD/)
- [GERGOVIA - Wine trading in Gergovia.](https://www.spoj.com/problems/GERGOVIA/)
- [Picking Up Chicks.](https://www.spoj.com/problems/GCJ101BB/)
- [CHOCOLA – Chocolate.](https://www.spoj.com/problems/CHOCOLA/)
- [ARRANGE - Arranging Amplifiers.](https://www.spoj.com/problems/ARRANGE/)
- [K Centers Problem.](https://www.geeksforgeeks.org/k-centers-problem-set-1-greedy-approximate-algorithm/)
- [Minimum Cost of ropes.](https://practice.geeksforgeeks.org/problems/minimum-cost-of-ropes/0)
- [Find smallest number with given number of digits and sum of digits.](https://practice.geeksforgeeks.org/problems/smallest-number5829/1)
- [Rearrange characters in a string such that no two adjacent are same.](https://practice.geeksforgeeks.org/problems/rearrange-characters/0)
- [Find maximum sum possible equal sum of three stacks.](https://www.geeksforgeeks.org/find-maximum-sum-possible-equal-sum-three-stacks/)

## • Backtracking

- [Rat in a maze Problem.](https://practice.geeksforgeeks.org/problems/rat-in-a-maze-problem/1)
- [Printing all solutions in N-Queen Problem.](https://www.geeksforgeeks.org/printing-solutions-n-queen-problem/)
- [Word Break Problem using Backtracking.](https://practice.geeksforgeeks.org/problems/word-break-part-2/0)
- [Remove Invalid Parentheses.](https://leetcode.com/problems/remove-invalid-parentheses/)
- [Sudoku Solver.](https://practice.geeksforgeeks.org/problems/solve-the-sudoku/0)
- [M Coloring Problem.](https://practice.geeksforgeeks.org/problems/m-coloring-problem/0)
- [Print all palindromic partitions of a string.](https://www.geeksforgeeks.org/given-a-string-print-all-possible-palindromic-partition/)
- [Subset Sum Problem.](https://practice.geeksforgeeks.org/problems/subset-sum-problem2014/1)
- [The Knight’s tour problem.](https://www.geeksforgeeks.org/the-knights-tour-problem-backtracking-1/)
- [Tug of War.](https://www.geeksforgeeks.org/tug-of-war/)
- [Find shortest safe route in a path with landmines.](https://www.geeksforgeeks.org/find-shortest-safe-route-in-a-path-with-landmines/)
- [Combinational Sum.](https://practice.geeksforgeeks.org/problems/combination-sum/0)
- [Find Maximum number possible by doing at-most K swaps.](https://practice.geeksforgeeks.org/problems/largest-number-in-k-swaps/0)
- [Print all permutations of a string.](https://practice.geeksforgeeks.org/problems/permutations-of-a-given-string/0)
- [Find if there is a path of more than k length from a source.](https://www.geeksforgeeks.org/find-if-there-is-a-path-of-more-than-k-length-from-a-source/)
- [Longest Possible Route in a Matrix with Hurdles.](https://www.geeksforgeeks.org/longest-possible-route-in-a-matrix-with-hurdles/)
- [Print all possible paths from top left to bottom right of a mXn matrix.](https://www.geeksforgeeks.org/print-all-possible-paths-from-top-left-to-bottom-right-of-a-mxn-matrix/)
- [Partition of a set intoK subsets with equal sum.](https://practice.geeksforgeeks.org/problems/partition-array-to-k-subsets/1)
- [Partition of a set into K subsets with equal sum.](https://practice.geeksforgeeks.org/problems/partition-array-to-k-subsets/1)
- [Find the K-th Permutation Sequence of first N natural numbers.](https://www.geeksforgeeks.org/find-the-k-th-permutation-sequence-of-first-n-natural-numbers/)

## • Stacks and Queues

- [Implement Stack from Scratch.](https://www.tutorialspoint.com/javaexamples/data_stack.htm)
- [Implement Queue from Scratch.](https://www.geeksforgeeks.org/queue-set-1introduction-and-array-implementation/)
- [Implement 2 stack in an array.](https://practice.geeksforgeeks.org/problems/implement-two-stacks-in-an-array/1)
- [Find the middle element of a stack.](https://www.geeksforgeeks.org/design-a-stack-with-find-middle-operation/)
- [Implement "K" stacks in an Array.](https://www.geeksforgeeks.org/efficiently-implement-k-stacks-single-array/)
- [Check the expression has valid or Balanced parenthesis or not.](https://practice.geeksforgeeks.org/problems/parenthesis-checker/0)
- [Reverse a String using Stack.](https://practice.geeksforgeeks.org/problems/reverse-a-string-using-stack/1)
- [Design a Stack that supports getMin() in O(1) time and O(1) extra space.](https://practice.geeksforgeeks.org/problems/special-stack/1)
- [Find the next Greater element.](https://practice.geeksforgeeks.org/problems/next-larger-element/0)
- [The celebrity Problem.](https://practice.geeksforgeeks.org/problems/the-celebrity-problem/1)
- [Arithmetic Expression evaluation.](https://www.geeksforgeeks.org/arithmetic-expression-evalution/#:~:text=The%20stack%20organization%20is%20very,i.e.%2C%20A%20%2B%20B)
- [Evaluation of Postfix expression.](https://practice.geeksforgeeks.org/problems/evaluation-of-postfix-expression/0)
- [Implement a method to insert an element at its bottom without using any other data structure.](https://stackoverflow.com/questions/45130465/inserting-at-the-end-of-stack)
- [Reverse a stack using recursion.](https://www.geeksforgeeks.org/reverse-a-stack-using-recursion/)
- [Sort a Stack using recursion.](https://practice.geeksforgeeks.org/problems/sort-a-stack/1)
- [Merge Overlapping Intervals.](https://practice.geeksforgeeks.org/problems/overlapping-intervals/0)
- [Largest rectangular Area in Histogram.](https://practice.geeksforgeeks.org/problems/maximum-rectangular-area-in-a-histogram/0)
- [Length of the Longest Valid Substring.](https://practice.geeksforgeeks.org/problems/valid-substring0624/1)
- [Expression contains redundant bracket or not.](https://www.geeksforgeeks.org/expression-contains-redundant-bracket-not/)
- [Implement Stack using Queue.](https://practice.geeksforgeeks.org/problems/stack-using-two-queues/1)
- [Implement Stack using Deque.](https://www.geeksforgeeks.org/implement-stack-queue-using-deque/)
- [Stack Permutations (Check if an array is stack permutation of other).](https://www.geeksforgeeks.org/stack-permutations-check-if-an-array-is-stack-permutation-of-other/)
- [Implement Queue using Stack.](https://practice.geeksforgeeks.org/problems/queue-using-two-stacks/1)
- [Implement "n" queue in an array.](https://www.geeksforgeeks.org/efficiently-implement-k-queues-single-array/)
- [Implement a Circular queue.](https://www.geeksforgeeks.org/circular-queue-set-1-introduction-array-implementation/)
- [LRU Cache Implementationa.](https://practice.geeksforgeeks.org/problems/lru-cache/1)
- [Reverse a Queue using recursion.](https://practice.geeksforgeeks.org/problems/queue-reversal/1)
- [Reverse the first “K” elements of a queue.](https://practice.geeksforgeeks.org/problems/reverse-first-k-elements-of-queue/1)
- [Interleave the first half of the queue with second half.](https://www.geeksforgeeks.org/interleave-first-half-queue-second-half/)
- [Find the first circular tour that visits all Petrol Pumps.](https://practice.geeksforgeeks.org/problems/circular-tour/1)
- [Minimum time required to rot all oranges.](https://practice.geeksforgeeks.org/problems/rotten-oranges/0)
- [Distance of nearest cell having 1 in a binary matrix.](https://practice.geeksforgeeks.org/problems/distance-of-nearest-cell-having-1/0)
- [First negative integer in every window of size “k”.](https://practice.geeksforgeeks.org/problems/first-negative-integer-in-every-window-of-size-k/0)
- [Check if all levels of two trees are anagrams or not.](https://www.geeksforgeeks.org/check-if-all-levels-of-two-trees-are-anagrams-or-not/)
- [Sum of minimum and maximum elements of all subarrays of size “k”.](https://www.geeksforgeeks.org/sum-minimum-maximum-elements-subarrays-size-k/)
- [Minimum sum of squares of character counts in a given string after removing “k” characters.](https://practice.geeksforgeeks.org/problems/game-with-string/0)
- [Queue based approach or first non-repeating character in a stream.](https://practice.geeksforgeeks.org/problems/first-non-repeating-character-in-a-stream/0)
- [Next Smaller Element.](https://www.geeksforgeeks.org/next-smaller-element/)

## • Heap

- [Implement a Maxheap/MinHeap using arrays and recursion.](https://www.geeksforgeeks.org/building-heap-from-array/)
- [Sort an Array using heap.](https://www.geeksforgeeks.org/heap-sort/)
- [Maximum of all subarrays of size k.](https://www.geeksforgeeks.org/sliding-window-maximum-maximum-of-all-subarrays-of-size-k/)
- [“k” largest element in an array.](https://practice.geeksforgeeks.org/problems/k-largest-elements4206/1)
- [Kth smallest and largest element in an unsorted array.](https://www.geeksforgeeks.org/kth-smallestlargest-element-unsorted-array/)
- [Merge “K” sorted arrays.](https://practice.geeksforgeeks.org/problems/merge-k-sorted-arrays/1)
- [Merge 2 Binary Max Heaps.](https://practice.geeksforgeeks.org/problems/merge-two-binary-max-heap/0)
- [Kth largest sum continuous subarrays.](https://www.geeksforgeeks.org/k-th-largest-sum-contiguous-subarray/)
- [Leetcode- reorganize strings.](https://leetcode.com/problems/reorganize-string/)
- [Merge “K” Sorted Linked Lists.](https://practice.geeksforgeeks.org/problems/merge-k-sorted-linked-lists/1)
- [Smallest range in “K” Lists.](https://practice.geeksforgeeks.org/problems/find-smallest-range-containing-elements-from-k-lists/1)
- [Median in a stream of Integers.](https://practice.geeksforgeeks.org/problems/find-median-in-a-stream/0)
- [Check if a Binary Tree is Heap.](https://practice.geeksforgeeks.org/problems/is-binary-tree-heap/1)
- [Connect “n” ropes with minimum cost.](https://practice.geeksforgeeks.org/problems/minimum-cost-of-ropes/0)
- [Convert BST to Min Heap.](https://www.geeksforgeeks.org/convert-bst-min-heap/)
- [Convert min heap to max heap.](https://www.geeksforgeeks.org/convert-min-heap-to-max-heap/)
- [Rearrange characters in a string such that no two adjacent are same.](https://practice.geeksforgeeks.org/problems/rearrange-characters/0)
- [Minimum sum of two numbers formed from digits of an array.](https://practice.geeksforgeeks.org/problems/minimum-sum4058/1)

## • Graph

- [Create a Graph, print it.](https://practice.geeksforgeeks.org/problems/bfs-traversal-of-graph/1)
- [Implement BFS algorithm.](https://practice.geeksforgeeks.org/problems/bfs-traversal-of-graph/1)
- [Implement DFS Algo.](https://www.geeksforgeeks.org/depth-first-search-or-dfs-for-a-graph/)
- [Detect Cycle in Directed Graph using BFS/DFS Algo.](https://www.geeksforgeeks.org/detect-cycle-in-a-graph/)
- [Detect Cycle in UnDirected Graph using BFS/DFS Algo.](https://practice.geeksforgeeks.org/problems/detect-cycle-in-an-undirected-graph/1)
- [Search in a Maze.](https://practice.geeksforgeeks.org/problems/rat-in-a-maze-problem/1)
- [Minimum Step by Knight.](https://practice.geeksforgeeks.org/problems/steps-by-knight/0)
- [Flood fill algo.](https://leetcode.com/problems/flood-fill/)
- [Clone a graph.](https://leetcode.com/problems/clone-graph/)
- [Making wired Connections.](https://leetcode.com/problems/number-of-operations-to-make-network-connected/)
- [word Ladder.](https://leetcode.com/problems/word-ladder/)
- [Dijkstra algo.](https://www.geeksforgeeks.org/dijkstras-shortest-path-algorithm-greedy-algo-7/)
- [Implement Topological Sort.](https://practice.geeksforgeeks.org/problems/topological-sort/1)
- [Minimum time taken by each job to be completed given by a Directed Acyclic Graph.](https://www.geeksforgeeks.org/minimum-time-taken-by-each-job-to-be-completed-given-by-a-directed-acyclic-graph/)
- [Find whether it is possible to finish all tasks or not from given dependencies.](https://www.geeksforgeeks.org/find-whether-it-is-possible-to-finish-all-tasks-or-not-from-given-dependencies/)
- [Find the no. of Isalnds.](https://practice.geeksforgeeks.org/problems/find-the-number-of-islands/1)
- [Given a sorted Dictionary of an Alien Language, find order of characters.](https://practice.geeksforgeeks.org/problems/alien-dictionary/1)
- [Implement Kruksal’s Algorithm.](https://www.geeksforgeeks.org/kruskals-minimum-ning-tree-algorithm-greedy-algo-2/)
- [Implement Prim’s Algorithm.](https://www.geeksforgeeks.org/prims-minimum-ning-tree-mst-greedy-algo-5/)
- [Total no. of Spanning tree in a graph.](https://www.geeksforgeeks.org/total-number-ning-trees-graph/)
- [Implement Bellman Ford Algorithm.](https://practice.geeksforgeeks.org/problems/negative-weight-cycle/0)
- [Implement Floyd Warshall Algorithm.](https://practice.geeksforgeeks.org/problems/implementing-floyd-warshall/0)
- [Travelling Salesman Problem.](https://www.geeksforgeeks.org/travelling-salesman-problem-set-1/)
- [Graph Colouring Problem.](https://www.geeksforgeeks.org/graph-coloring-applications/#:~:text=Graph%20coloring%20problem%20is%20to,are%20colored%20using%20same%20color.)
- [Snake and Ladders Problem.](https://leetcode.com/problems/snakes-and-ladders/)
- [Find bridge in a graph.](https://www.geeksforgeeks.org/bridge-in-a-graph/)
- [Count Strongly connected Components (Kosaraju Algo).](https://practice.geeksforgeeks.org/problems/strongly-connected-components-kosarajus-algo/1)
- [Check whether a graph is Bipartite or Not.](https://www.geeksforgeeks.org/bipartite-graph/)
- [Detect Negative cycle in a graph.](https://www.geeksforgeeks.org/detect-negative-cycle-graph-bellman-ford/)
- [Longest path in a Directed Acyclic Graph.](https://www.geeksforgeeks.org/find-longest-path-directed-acyclic-graph/)
- [Journey to the Moon.](https://www.hackerrank.com/challenges/journey-to-the-moon/problem)
- [Cheapest Flights Within K Stops.](https://leetcode.com/problems/cheapest-flights-within-k-stops/description/)
- [Oliver and the Game.](https://www.hackerearth.com/practice/algorithms/graphs/topological-sort/practice-problems/algorithm/oliver-and-the-game-3/)
- [Water Jug problem using BFS.](https://www.geeksforgeeks.org/water-jug-problem-using-bfs/)
- [Find if there is a path of more thank length from a source.](https://www.geeksforgeeks.org/find-if-there-is-a-path-of-more-than-k-length-from-a-source/)
- [M-Colouring Problem.](https://practice.geeksforgeeks.org/problems/m-coloring-problem/0)
- [Minimum edges to reverse o make path from source to destination.](https://www.geeksforgeeks.org/minimum-edges-reverse-make-path-source-destination/)
- [Paths to travel each nodes using each edge (Seven Bridges).](https://www.geeksforgeeks.org/paths-travel-nodes-using-edgeseven-bridges-konigsberg/)
- [Vertex Cover Problem.](https://www.geeksforgeeks.org/vertex-cover-problem-set-1-introduction-approximate-algorithm-2/)
- [Chinese Postman or Route Inspection.](https://www.geeksforgeeks.org/chinese-postman-route-inspection-set-1-introduction/)
- [Number of Triangles in a Directed and Undirected Graph.](https://www.geeksforgeeks.org/number-of-triangles-in-directed-and-undirected-graphs/)
- [Minimise the cashflow among a given set of friends who have borrowed money from each other.](https://www.geeksforgeeks.org/minimize-cash-flow-among-given-set-friends-borrowed-money/)
- [Two Clique Problem.](https://www.geeksforgeeks.org/two-clique-problem-check-graph-can-divided-two-cliques/)

## • Trie

- [Construct a trie from scratch.](https://www.geeksforgeeks.org/trie-insert-and-search/)
- [Find shortest unique prefix for every word in a given list.](https://www.geeksforgeeks.org/find-all-shortest-unique-prefixes-to-represent-each-word-in-a-given-list/)
- [Word Break Problem.](https://www.geeksforgeeks.org/word-break-problem-trie-solution/)
- [Given a sequence of words, print all anagrams together.](https://practice.geeksforgeeks.org/problems/k-anagrams-1/0)
- [Implement a Phone Directory.](https://practice.geeksforgeeks.org/problems/phone-directory/0)
- [Print unique rows in a given boolean matrix.](https://practice.geeksforgeeks.org/problems/unique-rows-in-boolean-matrix/1)

## • Dynamic Programming

- [Coin Change Problem.](https://practice.geeksforgeeks.org/problems/coin-change2448/1)
- [Knapsack Problem.](https://practice.geeksforgeeks.org/problems/0-1-knapsack-problem/0)
- [Binomial Coefficient Problem.](https://practice.geeksforgeeks.org/problems/ncr1019/1)
- [Permutation Coefficient Problem.](https://www.geeksforgeeks.org/permutation-coefficient/)
- [Program for nth Catalan Number.](https://www.geeksforgeeks.org/program-nth-catalan-number/)
- [Matrix Chain Multiplication.](https://www.geeksforgeeks.org/matrix-chain-multiplication-dp-8/)
- [Edit Distance.](https://practice.geeksforgeeks.org/problems/edit-distance3702/1)
- [Subset Sum Problem.](https://practice.geeksforgeeks.org/problems/subset-sum-problem2014/1)
- [Friends Pairing Problem.](https://practice.geeksforgeeks.org/problems/friends-pairing-problem5425/1)
- [Gold Mine Problem.](https://www.geeksforgeeks.org/gold-mine-problem/)
- [Assembly Line Scheduling Problem.](https://www.geeksforgeeks.org/assembly-line-scheduling-dp-34/)
- [Painting the Fence problem.](https://practice.geeksforgeeks.org/problems/painting-the-fence3727/1)
- [Maximize The Cut Segments.](https://practice.geeksforgeeks.org/problems/cutted-segments/0)
- [Longest Common Subsequence.](https://practice.geeksforgeeks.org/problems/longest-common-subsequence/0)
- [Longest Repeated Subsequence.](https://practice.geeksforgeeks.org/problems/longest-repeating-subsequence/0)
- [Longest Increasing Subsequence.](https://practice.geeksforgeeks.org/problems/longest-increasing-subsequence/0)
- [Space Optimized Solution of LCS.](https://www.geeksforgeeks.org/space-optimized-solution-lcs/)
- [LCS (Longest Common Subsequence) of three strings.](https://practice.geeksforgeeks.org/problems/lcs-of-three-strings/0)
- [Maximum Sum Increasing Subsequence.](https://practice.geeksforgeeks.org/problems/maximum-sum-increasing-subsequence4749/1)
- [Count all subsequences having product less than K.](https://www.geeksforgeeks.org/count-subsequences-product-less-k/)
- [Longest subsequence such that difference between adjacent is one.](https://practice.geeksforgeeks.org/problems/longest-subsequence-such-that-difference-between-adjacents-is-one4724/1)
- [Maximum subsequence sum such that no three are consecutive.](https://www.geeksforgeeks.org/maximum-subsequence-sum-such-that-no-three-are-consecutive/)
- [Egg Dropping Problem.](https://practice.geeksforgeeks.org/problems/egg-dropping-puzzle/0)
- [Maximum Length Chain of Pairs.](https://practice.geeksforgeeks.org/problems/max-length-chain/1)
- [Maximum size square sub-matrix with all 1s.](https://practice.geeksforgeeks.org/problems/largest-square-formed-in-a-matrix/0)
- [Maximum sum of pairs with specific difference.](https://practice.geeksforgeeks.org/problems/pairs-with-specific-difference/0)
- [Min Cost PathProblem.](https://practice.geeksforgeeks.org/problems/path-in-matrix3805/1)
- [Maximum difference of zeros and ones in binary string.](https://practice.geeksforgeeks.org/problems/maximum-difference-of-zeros-and-ones-in-binary-string4111/1)
- [Minimum number of jumps to reach end.](https://practice.geeksforgeeks.org/problems/minimum-number-of-jumps/0)
- [Minimum cost to fill given weight in a bag.](https://practice.geeksforgeeks.org/problems/minimum-cost-to-fill-given-weight-in-a-bag1956/1)
- [Minimum removals from array to make max –min <= K.](https://www.geeksforgeeks.org/minimum-removals-array-make-max-min-k/)
- [Longest Common Substring.](https://practice.geeksforgeeks.org/problems/longest-common-substring/0)
- [Count number of ways to reacha given score in a game.](https://practice.geeksforgeeks.org/problems/reach-a-given-score/0)
- [Count Balanced Binary Trees of Height h.](https://practice.geeksforgeeks.org/problems/bbt-counter/0)
- [Largest Sum Contiguous Subarray.](https://practice.geeksforgeeks.org/problems/kadanes-algorithm/0)
- [Smallest sum contiguous subarray.](https://www.geeksforgeeks.org/smallest-sum-contiguous-subarray/)
- [Unbounded Knapsack (Repetition of items allowed).](https://practice.geeksforgeeks.org/problems/knapsack-with-duplicate-items4201/1)
- [Word Break Problem.](https://practice.geeksforgeeks.org/problems/word-break/0)
- [Largest Independent Set Problem.](https://www.geeksforgeeks.org/largest-independent-set-problem-dp-26/)
- [Partition problem.](https://practice.geeksforgeeks.org/problems/subset-sum-problem2014/1)
- [Longest Palindromic Subsequence.](https://www.geeksforgeeks.org/longest-palindromic-subsequence-dp-12/)
- [Count All Palindromic Subsequence in a given String.](https://practice.geeksforgeeks.org/problems/count-palindromic-subsequences/1)
- [Longest Palindromic Substring.](https://leetcode.com/problems/longest-palindromic-substring/)
- [Longest alternating subsequence.](https://practice.geeksforgeeks.org/problems/longest-alternating-subsequence/0)
- [Weighted Job Scheduling.](https://www.geeksforgeeks.org/weighted-job-scheduling/)
- [Coin game winner where every player has three choices.](https://www.geeksforgeeks.org/coin-game-winner-every-player-three-choices/)
- [Count Derangements (Permutation such that no element appears in its original position).](https://www.geeksforgeeks.org/count-derangements-permutation-such-that-no-element-appears-in-its-original-position/)
- [Maximum profit by buying and selling a share at most twice.](https://www.geeksforgeeks.org/maximum-profit-by-buying-and-selling-a-share-at-most-twice/)
- [Optimal Strategy for a Game.](https://practice.geeksforgeeks.org/problems/optimal-strategy-for-a-game/0)
- [Optimal Binary Search Tree.](https://www.geeksforgeeks.org/optimal-binary-search-tree-dp-24/)
- [Palindrome PartitioningProblem.](https://practice.geeksforgeeks.org/problems/palindromic-patitioning4845/1)
- [Word Wrap Problem.](https://practice.geeksforgeeks.org/problems/word-wrap/0)
- [Mobile Numeric Keypad Problem.](https://practice.geeksforgeeks.org/problems/mobile-numeric-keypad5456/1)
- [Boolean Parenthesization Problem.](https://practice.geeksforgeeks.org/problems/boolean-parenthesization/0)
- [Largest rectangular sub-matrix whose sum is 0.](https://www.geeksforgeeks.org/largest-rectangular-sub-matrix-whose-sum-0/)
- [Largest area rectangular sub-matrix with equal number of 1’s and 0’s.](https://www.geeksforgeeks.org/largest-area-rectangular-sub-matrix-equal-number-1s-0s/)
- [Maximum sum rectangle in a 2D matrix.](https://practice.geeksforgeeks.org/problems/maximum-sum-rectangle/0)
- [Maximum profit by buying and selling a share at most k times.](https://practice.geeksforgeeks.org/problems/maximum-profit4657/1)
- [Find if a string is interleaved of two other strings.](https://practice.geeksforgeeks.org/problems/interleaved-strings/1)
- [Maximum Length of Pair Chain.](https://leetcode.com/problems/maximum-length-of-pair-chain/)

## • Bits Manipulation

- [Count set bits in an integer.](https://practice.geeksforgeeks.org/problems/set-bits0143/1)
- [Find the two non-repeating elements in an array of repeating elements.](https://practice.geeksforgeeks.org/problems/finding-the-numbers0215/1)
- [Count number of bits to be flipped to convert A to B.](https://practice.geeksforgeeks.org/problems/bit-difference/0)
- [Count total set bits in all numbers from 1 to n.](https://practice.geeksforgeeks.org/problems/count-total-set-bits/0)
- [Program to find whether a no is power of two.](https://practice.geeksforgeeks.org/problems/power-of-2/0)
- [Find position of the only set bit.](https://practice.geeksforgeeks.org/problems/find-position-of-set-bit3706/1)
- [Copy set bits in a range.](https://www.geeksforgeeks.org/copy-set-bits-in-a-range/)
- [Divide two integers without using multiplication, division and mod operator.](https://www.geeksforgeeks.org/divide-two-integers-without-using-multiplication-division-mod-operator/)
- [Calculate square of a number without using \*, / and pow().](<https://www.geeksforgeeks.org/calculate-square-of-a-number-without-using-and-pow/#:~:text=Given%20an%20integer%20n%2C%20calculate,*%2C%20%2F%20and%20pow().&text=A%20Simple%20Solution%20is%20to%20repeatedly%20add%20n%20to%20result.>)
- [Power Set.](https://practice.geeksforgeeks.org/problems/power-set4302/1)
