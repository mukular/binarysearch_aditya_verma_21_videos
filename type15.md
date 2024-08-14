# FIND PEAK ELEMENT IN AN ARRAY :-

# A peak element is an element that is greater than its neighbors.

# Given an input array nums, where nums[i] ≠ nums[i+1], find a peak element and return its index. The array may contain multiple peaks, in that case return the index to any one of the peaks is fine.You may imagine that nums[-1] = nums[n] = -∞.

Example :

Input: nums = [1,2,3,1]

Output: 2
> Explanation: 3 is a peak element and your function should return the index number 2.


```cpp
int low = 0;
int high = size - 1;

while(low <= high)
{
    int mid = low + (high - low)/2;

    if(mid > 0 && mid < size - 1)
    {
        if(arr[mid] > arr[mid-1] && arr[mid] > arr[mid+1])
        {
            return mid;
        }
        else if(arr[mid-1] > arr[mid])
        {
            high = mid - 1;
        }
        else
        {
            low = mid + 1;
        }
    }
    else if(mid == 0)
    {
        if(arr[0] > arr[1])
        {
            return 0;
        }
        else
        {
            return 1;
        }
    }
    else if(mid == size-1)
    {
        if(arr[size-1] > arr[size-2])
        {
            return size-1;
        }
        else
        {
            return size-2;
        }
    }
}

```