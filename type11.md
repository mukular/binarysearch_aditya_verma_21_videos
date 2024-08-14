# Next letter :-

# Given an array of letters sorted in ascending order, find the smallest letter in the the array which is greater than a given key letter. . 

Ex. arr = [a, c, f, h], key = f

Output:- h

```cpp

// Binary Search ke code me yeh conditions change karni h

char res = '#';

if(arr[mid] == key)
{
    start = mid + 1;
}
else if(arr[mid] < key)
{
    start = mid + 1;
}
else if(arr[mid] > key)
{
    res = arr[mid];
    end = mid - 1;
}

// agar res = '#' h abhi bhi toh iska matlab koi mila hi nhi

return res;

```