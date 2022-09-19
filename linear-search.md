# Linear Search Algorithm 🔎

`Linear Search` is defined as a sequential search algorithm that starts at one end and goes through each element of a list until the desired element is found, otherwise the search continues till the end of the data set. It is the easiest searching algorithm.

![linear-search-image](https://media.geeksforgeeks.org/wp-content/cdn-uploads/Linear-Search.png)

Given an array arr[] of N elements, the task is to write a function to search a given element x in arr[].

```
Input: arr[] = {10, 20, 80, 30, 60, 50,110, 100, 130, 170}, x = 110;
Output: 6
Explanation: Element x is present at index 6

Input: arr[] = {10, 20, 80, 30, 60, 50,110, 100, 130, 170}, x = 175;
Output: -1
Explanation: Element x is not present in arr[].
```

---

### Follow the below `idea` to solve the problem:

```
Iterate from 0 to N-1 and compare the value of every index with x if they match return index
```

---

### Follow the given steps to solve the problem:

- Start from the leftmost element of arr[] and one by one compare x with each element of arr[]
- If x matches with an element, return the index.
- If x doesn’t match with any of the elements, return -1.
- Below is the implementation of the above approach:

---

```
// Javascript code to linearly search x in arr[]. If x
// is present then return its location, otherwise
// return -1

function search(arr, n, x)
{
    let i;
    for (i = 0; i < n; i++)
        if (arr[i] == x)
            return i;
    return -1;
}

// Driver code

    let arr = [ 2, 3, 4, 10, 40 ];
    let x = 10;
    let n = arr.length;

    // Function call
    let result = search(arr, n, x);
    (result == -1)
        ? document.write("Element is not present in array")
        : document.write("Element is present at index " + result);

// This code is contributed by Manoj
```

---

Output;

```
Element is present at index 3

Time complexity: O(N)
Auxiliary Space: O(1)
```
