# Minimum difference element in a sorted array :-

# Given a sorted array, find the element in the array which has minimum absolute difference with the given number. 

Ex. arr = [1, 3, 8, 10, 15], key = 12

Output :- 10

```cpp

int low = 0;
int high = size - 1;

while(low <= high)
{
    int mid = low + (high - low)/2;

    if(ele == arr[mid])
    {
        return arr[mid];
    }
    else if(ele < arr[mid])
    {
        high = mid - 1;
    }
    else
    {
        low = mid + 1;
    }
}

// Now find abs(arr[low] - key) and abs(arr[high] - key) and compare with each other. 

// If abs(arr[low] - key) is minimum then return arr[low] else return arr[high].

```