'''You are given an integer array nums and an integer k.

In one operation, you can choose any index i where 0 <= i < nums.length and change nums[i] to nums[i] + x where x is an integer from the range [-k, k]. You can apply this operation at most once for each index i.

The score of nums is the difference between the maximum and minimum elements in nums.

Return the minimum score of nums after applying the mentioned operation at most once for each index in it.

Example 1:
Input: nums = [1], k = 0
Output: 0

Explanation: The score is max(nums) - min(nums) = 1 - 1 = 0.'''
def min_score_after_operation(nums, k):
    # Step 1: Find the minimum and maximum elements in the original array
    original_min = min(nums)
    original_max = max(nums)
    
    # Step 2: Find the potential minimum and maximum elements
    potential_min = original_min
    potential_max = original_max
    for num in nums:
        potential_min = min(num - k, potential_min)
        potential_max = max(num + k, potential_max)
    
    # Step 3: Calculate the scores
    original_score = original_max - original_min
    potential_score = potential_max - potential_min
    
    # Step 4: Return the minimum score
    return min(original_score, potential_score)

# Example usage
nums = [1]
k = 0
print(min_score_after_operation(nums, k))  # Output: 0
