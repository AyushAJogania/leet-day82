# leet-day82

# Majority Element

This C++ program finds the majority element in an array. The majority element is defined as an element that appears more than ⌊n / 2⌋ times in the array, where n is the size of the array.

## Problem Statement

Given an integer array `nums` of size n, find the majority element. You may assume that the majority element always exists in the array.

### Example

**Input:**
```
nums = [3, 2, 3]
```

**Output:**
```
3
```

**Input:**
```
nums = [2, 2, 1, 1, 1, 2, 2]
```

**Output:**
```
2
```

### Constraints

- n == nums.length
- 1 <= n <= 5 * 10^4
- -10^9 <= nums[i] <= 10^9

## Approach

We can solve this problem using the Boyer-Moore Majority Vote algorithm, which has a time complexity of O(n) and uses constant space.

The algorithm works as follows:
1. Initialize two variables, `majority` and `count`, to keep track of the majority candidate and its count.
2. Iterate through the array from left to right.
3. For each element in the array:
   - If the `count` is 0, set the current element as the `majority` candidate and reset the `count` to 1.
   - If the current element is the same as the `majority` candidate, increment the `count`.
   - If the current element is different from the `majority` candidate, decrement the `count`.
4. The `majority` variable will hold the majority element after the iteration.

## How to Use

1. Clone this repository to your local machine.
2. Open the project in your preferred C++ development environment.
3. Modify the `nums` vector in the `main` function to contain the input array.
4. Compile and run the program.
5. The program will output the majority element.

## Example

```cpp
#include <iostream>
#include <vector>

class Solution {
public:
    int majorityElement(std::vector<int>& nums) {
        int majority = nums[0];  // Initialize the majority candidate
        int count = 1;          // Initialize the count of the majority candidate
        
        for (int i = 1; i < nums.size(); i++) {
            if (count == 0) {
                majority = nums[i];  // Update the majority candidate
                count = 1;           // Reset the count
            } else if (nums[i] == majority) {
                count++;             // Increment the count if the current element is the majority candidate
            } else {
                count--;             // Decrement the count if the current element is not the majority candidate
            }
        }
        
        return majority;
    }
};


```

