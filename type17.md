# FIND AN ELEMENT IN BITONIC ARRAY :-

# Given a bitonic sequence of n distinct elements, write a program to find a given element x in the bitonic sequence in O(log n) time. A Bitonic Sequence is a sequence of numbers which is first strictly increasing then after a point strictly decreasing.

Examples:

Input :  arr[] = {-3, 9, 18, 20, 17, 5, 1};
         key = 20

Output : Found at index 3

```cpp

// First find index of max element using binary search as in previous problem let's say it is index

// Now apply BinarySearch(arr, 0, index-1, ascending)

// Now apply BinarySearch(arr, index, size-1, descending)

```
