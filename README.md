# LEETCODE-Array-75
Sure, let's do a dry run of the given `sortColors` method, which appears to implement the Bubble Sort algorithm. We'll go through an example step-by-step to understand how the algorithm sorts the array. Let's use the input array `nums = [2, 0, 2, 1, 1, 0]` for this dry run.

### Initial Array
```
nums = [2, 0, 2, 1, 1, 0]
```

### Outer Loop (i-loop)
The outer loop runs from `i = 0` to `n-1`. For each iteration of the outer loop, the largest unsorted element is "bubbled" to its correct position at the end of the array.

#### First Iteration (i = 0)
- **Inner Loop (j-loop)**: Runs from `j = 0` to `j = n-i-2` (i.e., 0 to 4)
    - Compare `nums[0]` (2) and `nums[1]` (0), since 2 > 0, swap them.
      ```
      nums = [0, 2, 2, 1, 1, 0]
      ```
    - Compare `nums[1]` (2) and `nums[2]` (2), no swap needed.
      ```
      nums = [0, 2, 2, 1, 1, 0]
      ```
    - Compare `nums[2]` (2) and `nums[3]` (1), since 2 > 1, swap them.
      ```
      nums = [0, 2, 1, 2, 1, 0]
      ```
    - Compare `nums[3]` (2) and `nums[4]` (1), since 2 > 1, swap them.
      ```
      nums = [0, 2, 1, 1, 2, 0]
      ```
    - Compare `nums[4]` (2) and `nums[5]` (0), since 2 > 0, swap them.
      ```
      nums = [0, 2, 1, 1, 0, 2]
      ```

#### Second Iteration (i = 1)
- **Inner Loop (j-loop)**: Runs from `j = 0` to `j = n-i-2` (i.e., 0 to 3)
    - Compare `nums[0]` (0) and `nums[1]` (2), no swap needed.
      ```
      nums = [0, 2, 1, 1, 0, 2]
      ```
    - Compare `nums[1]` (2) and `nums[2]` (1), since 2 > 1, swap them.
      ```
      nums = [0, 1, 2, 1, 0, 2]
      ```
    - Compare `nums[2]` (2) and `nums[3]` (1), since 2 > 1, swap them.
      ```
      nums = [0, 1, 1, 2, 0, 2]
      ```
    - Compare `nums[3]` (2) and `nums[4]` (0), since 2 > 0, swap them.
      ```
      nums = [0, 1, 1, 0, 2, 2]
      ```

#### Third Iteration (i = 2)
- **Inner Loop (j-loop)**: Runs from `j = 0` to `j = n-i-2` (i.e., 0 to 2)
    - Compare `nums[0]` (0) and `nums[1]` (1), no swap needed.
      ```
      nums = [0, 1, 1, 0, 2, 2]
      ```
    - Compare `nums[1]` (1) and `nums[2]` (1), no swap needed.
      ```
      nums = [0, 1, 1, 0, 2, 2]
      ```
    - Compare `nums[2]` (1) and `nums[3]` (0), since 1 > 0, swap them.
      ```
      nums = [0, 1, 0, 1, 2, 2]
      ```

#### Fourth Iteration (i = 3)
- **Inner Loop (j-loop)**: Runs from `j = 0` to `j = n-i-2` (i.e., 0 to 1)
    - Compare `nums[0]` (0) and `nums[1]` (1), no swap needed.
      ```
      nums = [0, 1, 0, 1, 2, 2]
      ```
    - Compare `nums[1]` (1) and `nums[2]` (0), since 1 > 0, swap them.
      ```
      nums = [0, 0, 1, 1, 2, 2]
      ```

#### Fifth Iteration (i = 4)
- **Inner Loop (j-loop)**: Runs from `j = 0` to `j = n-i-2` (i.e., 0 to 0)
    - Compare `nums[0]` (0) and `nums[1]` (0), no swap needed.
      ```
      nums = [0, 0, 1, 1, 2, 2]
      ```

### Sorted Array
```
nums = [0, 0, 1, 1, 2, 2]
```

### Conclusion
The `sortColors` method correctly sorts the array using the Bubble Sort algorithm. Each element is compared with its neighbor, and swaps are made when necessary, iteratively bubbling the largest unsorted element to the end of the array. The process repeats until the entire array is sorted.
