# Find the Rotation Count in Rotated Sorted array :-

# Consider an array of distinct numbers sorted in increasing order. The array has been rotated (clockwise) k number of times. Given such an array, find the value of k.

Examples:

Input : arr[] = {15, 18, 2, 3, 6, 12}

Output: 2

> Explanation : Initial array must be {2, 3, 6, 12, 15, 18}. We get the given array after rotating the initial array twice.

Input : arr[] = {7, 9, 11, 12, 5}

Output: 4

Input: arr[] = {7, 9, 11, 12, 15}

Output: 0

```cpp

// first check if arr[0] > last element of array then array is rotated

while(start <= end)
{
    find mid

    next = (mid + 1) % size
    prev = (mid + size - 1) % size

    if(arr[mid] <= arr[next] && arr[mid] <= arr[prev])
    {
        return mid;
    }

    if(arr[start] <= arr[mid])
    {
        start = mid + 1;
    }
    else if(arr[mid] <= arr[end])
    {
        end = mid - 1;
    }
}
```