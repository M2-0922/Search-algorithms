# Binary Search Algorithm 🔎

`Binary Search` is a searching algorithm used in a sorted array by repeatedly dividing the search interval in half. The idea of binary search is to use the information that the array is sorted and reduce the time complexity to O(Log n).

![binary-search-image](https://media.geeksforgeeks.org/wp-content/uploads/20220309171621/BinarySearch.png)

---

Given an array arr[] of N elements, the task is to write a function to search a given element x in arr[].

```
Input: arr[] = {10, 20, 30, 50, 60, 80, 110, 130, 140, 170}, x = 110
Output: 6
Explanation: Element x is present at index 6.

Input: arr[] = {10, 20, 30, 40, 60, 110, 120, 130, 170}, x = 175
Output: -1
Explanation: Element x is not present in arr[].
```

---

### Binary Search Algorithm: The basic steps to perform Binary Search are:

- Begin with the mid element of the whole array as a search key.
- If the value of the search key is equal to the item then return an index of the search key.
- Or if the value of the search key is less than the item in the middle of the interval, narrow the interval to the lower half.
- Otherwise, narrow it to the upper half.
- Repeatedly check from the second point until the value is found or the interval is empty.

---

### Binary Search Algorithm can be implemented in the following two ways

- Iterative Method
- Recursive Method

---

1. Iteration Method

```
binarySearch(arr, x, low, high)
        repeat till low = high
               mid = (low + high)/2
                   if (x == arr[mid])
                   return mid

                   else if (x > arr[mid]) // x is on the right side
                       low = mid + 1

                   else                  // x is on the left side
                       high = mid - 1
```

---

2. Recursive Method (The recursive method follows the divide and conquers approach)

```
    binarySearch(arr, x, low, high)
           if low > high
               return False

           else
               mid = (low + high) / 2
                   if x == arr[mid]
                   return mid

               else if x > arr[mid]        // x is on the right side
                   return binarySearch(arr, x, mid + 1, high)

               else                        // x is on the right side
                   return binarySearch(arr, x, low, mid - 1)
```

---

### `JS`;

```
function binarySearch(arr, l, r, x){
    if (r >= l) {
        let mid = l + Math.floor((r - l) / 2);

        // If the element is present at the middle
        // itself
        if (arr[mid] == x)
            return mid;

        // If element is smaller than mid, then
        // it can only be present in left subarray
        if (arr[mid] > x)
            return binarySearch(arr, l, mid - 1, x);

        // Else the element can only be present
        // in right subarray
        return binarySearch(arr, mid + 1, r, x);
    }

    // We reach here when element is not
    // present in array
    return -1;
}

let arr = [ 2, 3, 4, 10, 40 ];
let x = 10;
let n = arr.length
let result = binarySearch(arr, 0, n - 1, x);
(result == -1) ? document.write( "Element is not present in array")
                   : document.write("Element is present at index " +result);

```
