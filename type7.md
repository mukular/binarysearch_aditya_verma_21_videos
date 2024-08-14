# FIND AN ELEMENT IN A ROTATED SORTED ARRAY :-

# Suppose an array sorted in ascending order is rotated at some pivot unknown to you beforehand. (i.e., [0,1,2,4,5,6,7] might become [4,5,6,7,0,1,2]). You are given a target value to search. If found in the array return its index, otherwise return -1.You may assume no duplicate exists in the array.

## Your algorithm's runtime complexity must be in the order of O(log n).

Example:

Input: nums = [4,5,6,7,0,1,2], target = 0

Output: 4

```cpp

// Find index of pivot element(smallest element) , let's say it is index
// Then apply BinarySearch(arr, 0, index-1) 
// Then apply BinarySearch(arr, index, size-1)

// Then among both answers , the answer which is not -1 should be returned.
// If both BinarySearch returns -1 then it means element is not present in array.

```