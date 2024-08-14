# FIND FIRST AND LAST POSITIONS OF AN ELEMENT IN A SORTED ARRAY :-

# Given a sorted array with possibly duplicate elements, the task is to find indexes of first and last occurrences of an element x in the given array.

Example:

Input : arr[] = {1, 3, 5, 5, 5, 5 ,67, 123, 125}    
        x = 5

Output : 
> First Occurrence = 2

> Last Occurrence = 5

```cpp

// Code for first occurence
int start = 0;
int end = size - 1;
int res = -1;

while(start <= end)
{
    int mid = start + (end - start)/2;

    if(ele == arr[mid])
    {
        res = mid;
        end = mid - 1;
    }
    else if(ele < arr[mid])
    {
        end = mid - 1;
    }
    else
    {
        start = mid + 1;
    }

    return res;
}

// Code for last occurence
int start = 0;
int end = size - 1;
int res = -1;

while(start <= end)
{
    int mid = start + (end - start)/2;

    if(ele == arr[mid])
    {
        res = mid;
        start = mid + 1;
    }
    else if(ele < arr[mid])
    {
        end = mid - 1;
    }
    else
    {
        start = mid + 1;
    }

    return res;
}
```