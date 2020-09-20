# Easy Questions

### Two Sum
  
  **Notes**
  - There can be duplicate elements
  - Cannot use the same element twice (need to check whether index found in hash table is same as current index.
  
  **Key Algo**
  - Can be done in one pass. 
  - Iterate through array of nums, adding each to a hashmap with key being the element, and value being the index.
  - Before adding, check each time if target - nums[i] exists in the hash table. 
  - If it exists, we break. 

### Reorder Data in Log Files
  
  **Notes**
  - Sort letter-logs lexicographically.
  - Digit-logs should remain stable. Java Collections/Array.sort() automatically ensures stability.
  
  **Key Algo**
  - Design a custom comparator. Remember that in compare(o1, o2), for the o1 < o2 conditional we should return -1 if sorting in ascending order.
  - Can sort entire logs[] array in place by simply returning 0 if we detect that a particular log is a digit log. 
  - Perform String.split(" ") to separate identifier and words in log.
  
### Maximum Subarray
  **Key Algo**
  
  - *Solution 1: Standard one-pass*

    - At every element, check which is higher, the new sum or the new element itself.
    - If the new element is higher than the new sum, it means we are losing the max possible sum. In this case, set current sum to new element.
    - Else set current sum to new sum.
    - If current sum is higher than max, set max to current sum.
    - We are ensuring that just because current sum drops below new sum, it doesn't mean that this subarray can't be part of the maximum sum.
    - In this algo, we automatically handle the case where our current sum is negative, and the new element is higher than this negative. In this case we wouldn't want the negative portion of the current sum anymore because its lowering our maximum sum value. So we set current sum to the new element itself.
    
  - *Solution 2: Kadane's Algorithm*
    - No real difference between these solutions, just that in this case we use Dynamic Programming to keep track of the previous max sums so far. 

### Merge Two Sorted Lists
  **Notes**
  
  - For returning a new linked list's head even after adding elements further down the list, use the following code to initialize the new linked list:
  `ListNode res = new ListNode();
  ListNode initHead = res;
    
  // Add new nodes to res.next, doing res = res.next in each iteration
  // At the end, do the following to return the head
    
  return initHead.next;`
  
  **Key Algo**
  
  - Same code as a standard merge operation of merge sort. 
  - Since we are required to splice the two lists, we can directly assign l1 or l2 to res.next.

### Valid Parentheses
  **Notes**
  
  - Can't use a stack 
### 
