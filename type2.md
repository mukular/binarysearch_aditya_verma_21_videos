# In this problem, we have an array sorted in descending order and we want to find index of an element e within this array. Binary search in every step picks the middle element (m) of the array and compares it to e. If these elements are equal, than it returns the index of m. If e is greater than m, than e must be located in the left subarray. On the contrary, if m greater than e, e must be located in the right subarray. At this moment binary search repeats the step on the respective subrarray.

Ex. arr = [20 , 17, 15, 14, 13, 12, 10, 9, 8, 4], e = 4



## Because the algoritm splits in every step the array in half (and one half of the array is never processed) the input element must be located (or determined missing) in at most $ \log_2(n) $ steps.
---

```cpp

// change the following code only in previous code

if(ele < arr[mid])
{
    start = mid + 1;
}
else
{
    end = mid - 1;
}

```