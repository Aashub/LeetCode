# 1. Two Sum

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

## Approach
## Approach
This solution uses a brute-force approach with two nested loops.
For each element in the array, it checks every other element to see
if their sum equals the target value, while ensuring the same index
is not used twice.

Once a valid pair is found, the indices are stored and the loops exit
early to avoid unnecessary iterations.

## Complexity
Time: O(n²)  
Space: O(1)

## Code
```py
class Solution(object):
    def twoSum(self, nums, target):

        list = []

        # this nested for loop will help in iterate of each value and their index
        for index, value_i in enumerate(nums):
            for jndex, value_j in enumerate(nums):
                
                # if index value and actual value of both for loop will be same than it will skip this cycle
                if index == jndex and value_i == value_j:
                    pass

                # otherwise it will check that sum of first for loop value and second for loop value
                #is equal to target value eqvivalent or not.
                elif value_i + value_j == target:
                    

                  list.append(index)
                  list.append(jndex)
                
                # if list length is equal to two than loop will get break.
                if len(list) == 2:
                    break
        return list


sol = Solution()

sol.twoSum([3,2,4], 6)

```py
