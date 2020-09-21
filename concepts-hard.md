# Hard Questions
## Trapping Rain Water

**Key Algos**

- *Solution 1: Brute Force*

  - For every element in the array, find the maximum height in the left, and in the right.
  - We are basically finding how much water can be stored above the current element.
  - Water = min(rightMax, leftMax) - height[i]
  - Time complexity: O(n^2), Space complexity: O(1)

- *Solution 2: Dynamic Programming*

  - This solution is similar to Kadane's algorithm for finding the maximum subarray sum in an array. For each index, we store the maximum up till that point so far. 
  - This takes two iterations through the array. For creating the array of left maxes, we just iterate from left to right, keeping track of the maximum, and storing the updated maximum value in the indexes of the leftMax array.
  - For the rightMax array, we perform the same procedure but iterate backwards.
  - We then perform one final iteration through the height array to calculate the amount of water that can be stored above each element (same formula as Solution 1).
  - Time complexity: O(n), Space complexity: O(n)
  
- *Solution 3: Stacks*

  - 
