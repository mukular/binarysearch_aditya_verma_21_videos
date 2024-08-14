# Binary Search:-

# Given a sorted array arr[] of n elements, write a function to search a given element x in arr[]. 

# Binary Search: Search a sorted array by repeatedly dividing the search interval in half. Begin with an interval covering the whole array. If the value of the search key is less than the item in the middle of the interval, narrow the interval to the lower half. Otherwise narrow it to the upper half. Repeatedly check until the value is found or the interval is empty.

Ex. arr = [1 2 3 4 5 6 7 8 9, 10],  ele = 2

Output:- 1

# We have to return index of ele in arr
---

Time Complexity = $ \log_2(n) $


```cpp

int start = 0;
int end = size - 1;

while(start <= end)
{
    int mid = start + (end - start)/2;

    if(ele == arr[mid])
    {
        return mid;
    }
    else if(ele < arr[mid])
    {
        end = mid - 1;
    }
    else
    {
        start = mid + 1;
    }
}

```