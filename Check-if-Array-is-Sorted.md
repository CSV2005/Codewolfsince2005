# Check if the Array Is Sorted

## Problem

Given an array `arr` of size `n`, determine whether the array is sorted in ascending (non-decreasing) order.

- Return `true` if the array is sorted.
- Return `false` otherwise.

## Java Solution

```java
class Solution {
    boolean arraySortedOrNot(int[] arr, int n) {
        for (int i = 1; i < n; i++) {
            if (arr[i] < arr[i - 1]) {
                return false;
            }
        }
        return true;
    }
}
```

## Explanation

1. Start from index `1`, because each element is compared with the previous element.
2. If `arr[i] < arr[i - 1]`, the current element is smaller than the previous one, so the array is not sorted. Return `false`.
3. If the loop finishes without finding any such pair, return `true`.

Equal adjacent values are allowed because the array must be in **non-decreasing** order.

## Examples

### Example 1

**Input:** `arr = [1, 2, 3, 4, 5]`, `n = 5`  
**Output:** `true`

### Example 2

**Input:** `arr = [1, 2, 2, 3, 4]`, `n = 5`  
**Output:** `true`

### Example 3

**Input:** `arr = [1, 3, 2, 4, 5]`, `n = 5`  
**Output:** `false`

## Complexity Analysis

- **Time Complexity:** `O(n)` in the worst case, because each element is checked once.
- **Auxiliary Space Complexity:** `O(1)`, because the algorithm uses only a constant amount of extra space.
