# CEILING OF AN ELEMENT IN A SORTED ARRAY :-

# Given a sorted array and a value x, the ceiling of x is the smallest element in array greater than or equal to x, and the floor is the greatest element smaller than or equal to x. Assume that the array is sorted in non-decreasing order. Write efficient functions to find ceiling of x.

Examples :

For example, let the input array be {1, 2, 8, 10, 10, 12, 19}

For x = 0:    floor doesn't exist in array,  ceil  = 1

For x = 1:    floor  = 1,  ceil  = 1

For x = 5:    floor  = 2,  ceil  = 8

For x = 20:   floor  = 19,  ceil doesn't exist in array

```cpp

// Binary Search ke code me yeh conditions change kar deni h

if(arr[mid] == ele)
{
    return arr[mid];
}
else if(arr[mid] < key)
{
    start = mid + 1;
}
else
{
    res = arr[mid];
    end = mid - 1;
}

```