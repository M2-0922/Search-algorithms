# Search Algorithms 🔎

## Linear Search Algorithm

[Click here to check Linear Search 👈🏻](linear-search.md)

## Binary Search Algorithm

[Click here to check Binary Search! 👈🏻](binary-search.md)

## Linear Search vs Binary Search

Linear Searh Algorithm;

```
function search(arr, n, x)
{
    let i;
    for (i = 0; i < n; i++)
        if (arr[i] == x)
            return i;
    return -1;
}
```

Binary Search Algorithm;

```
function binarySearch(arr, l, r, x){
    if (r >= l) {
        let mid = l + Math.floor((r - l) / 2);

        if (arr[mid] == x)
            return mid;

        if (arr[mid] > x)
            return binarySearch(arr, l, mid - 1, x);

        return binarySearch(arr, mid + 1, r, x);
    }
    return -1;
}
```

---

<table>
    <tbody>
        <tr>
            <td>
                <p style="text-align:center"><strong>Linear Search&nbsp;</strong></p>
                <div style="min-height:12px;text-align:center" id="GFG_AD_Desktop_MTF_Postcontent_728x90"></div>
            </td>
            <td>
                <p style="text-align:center"><strong>Binary Search</strong></p>
                <div style="min-height:12px;text-align:center" id="GFG_AD_Desktop_MTF_Postcontent_728x90"></div>
            </td>
        </tr>
        <tr>
            <td>In linear search input data need not to be in sorted.</td>
            <td>In binary search input data need to be in sorted order.</td>
        </tr>
        <tr>
            <td>It is also called sequential search.</td>
            <td>It is also called half-interval search.</td>
        </tr>
        <tr>
            <td>The time complexity of linear search <strong>O(n)</strong>.&nbsp;</td>
            <td>The time complexity of binary search<strong> O(log n)</strong>.</td>
        </tr>
        <tr>
            <td>Multidimensional array can be used.</td>
            <td>Only single dimensional array is used.</td>
        </tr>
        <tr>
            <td>Linear search performs&nbsp;equality comparisons</td>
            <td>Binary search performs ordering comparisons</td>
        </tr>
        <tr>
            <td>It is less complex.</td>
            <td>It is more complex.</td>
        </tr>
        <tr>
            <td>It is very slow process.</td>
            <td>It is very fast process.</td>
        </tr>
    </tbody>
</table>

---

Linear Search
![linear-search-image-2](https://media.geeksforgeeks.org/wp-content/uploads/Linear.png)

Binary Search
![binary-search-image-2](https://media.geeksforgeeks.org/wp-content/uploads/binary-3.png)
