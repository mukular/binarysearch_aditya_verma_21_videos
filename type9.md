# FIND FLOOR OF AN ELEMENT IN A SORTED ARRAY :-

# Given a sorted array and a value x, the floor of x is the largest element in array smaller than or equal to x. Write efficient functions to find floor of x.

Example:

Input : arr[] = {1, 2, 8, 10, 10, 12, 19}, x = 5

Output : 2

> 2 is the largest element in arr[] smaller than 5.

```cpp

// Binary Search ke code me yeh conditions change kar deni h

if(arr[mid] == ele)
{
    return arr[mid];
}
if(arr[mid] < ele)
{
    res = arr[mid];
    start = mid + 1;
}
else if(arr[mid] > ele)
{
    end = mid - 1;
}

return res;

```