Number of Good Pairs
Problem Statement
Given an array of integers nums, a pair (i, j) is called a good pair if:

nums[i] == nums[j]
i < j
Return the number of good pairs in the array.

Example 1
Input:


text
nums = [1,2,3,1,1,3]
Output:


text
4
Explanation:

The good pairs are:

(0, 3) because nums[0] == nums[3] == 1
(0, 4) because nums[0] == nums[4] == 1
(3, 4) because nums[3] == nums[4] == 1
(2, 5) because nums[2] == nums[5] == 3
Therefore, the total number of good pairs is 4.

Approach: Hash Map
We can solve this problem efficiently using a hash map to count the frequency of each number.

Algorithm
Initialize a variable count = 0 to store the number of good pairs.
Create a hash map to store the frequency of each number.
Iterate through the array.
For each number, add its current frequency in the hash map to count. Each previous occurrence forms a good pair with the current number.
Increment the frequency of the current number in the hash map.
Return count.
