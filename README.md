# Median-of-Two-Sorted-Arrays
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.  The overall run time complexity should be O(log (m+n)).

The provided code implements the solution to the problem of finding the median of two sorted arrays. It utilizes the concept of binary search to efficiently locate the partition point in both arrays such that the elements on the left side of the partition are smaller than the elements on the right side.

Here's a breakdown of the approach:

1. Ensure nums1 is not longer than nums2. This simplifies the problem and makes sure we only need to perform binary search on one array.

2. Perform binary search on the shorter array (`nums1`) to find the correct partition such that elements on the left side are less than or equal to elements on the right side.

3. Calculate the median based on the partition. If the combined length of both arrays is odd, return the maximum of the left partition. If it's even, calculate the average of the maximum of the left partition and the minimum of the right partition.

Here's the step-by-step execution for each test case:

For `nums1 = [1, 3]` and `nums2 = [2]`:
- m = 2, n = 1, so we select nums1 as the shorter array.
- i = 1, j = 1, nums1[i-1] = 1, nums2[j] = 2. Both conditions are satisfied.
- max_of_left = max(1, 2) = 2
- min_of_right = min(3, None) = 3
- Median = (2 + 3) / 2 = 2.5

For `nums1 = [1, 2]` and `nums2 = [3, 4]`:
- m = 2, n = 2. Both arrays are of equal length.
- i = 1, j = 1, nums1[i-1] = 1, nums2[j] = 3. Both conditions are satisfied.
- max_of_left = max(1, 3) = 3
- min_of_right = min(2, 4) = 2
- Median = (3 + 2) / 2 = 2.5

The output matches the expected results. Hence, the code appears to be correct.
