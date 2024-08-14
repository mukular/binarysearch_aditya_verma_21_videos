# SEARCH IN A ROW WISE AND COLUMN WISE SORTED MATRIX :-

# Given an n x n matrix and a number x, find the position of x in the matrix if it is present in it. Otherwise, print “Not Found”. In the given matrix, every row and column is sorted in increasing order. The designed algorithm should have linear time complexity.

Time Complexity = O(n+m) where n and m are number of rows and columns

---
Example :

Input : mat[4][4] = 

                {{10, 20, 30, 40},
                  {15, 25, 35, 45},
                  {27, 29, 37, 48},
                  {32, 33, 39, 50}};

              x = 29

Output : Found at (2, 1)

```cpp

int i = 0;
int j = m-1;

while(i >= 0 && i < n && j >= 0 && j < m)
{
    if(arr[i][j] == key)
    {
        return whatever you have asked;
    }
    else if(arr[i][j] > key)
    {
        j--;
    }
    else if(arr[i][j] < key)
    {
        i++;
    }
}

return -1;

```