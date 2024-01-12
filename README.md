# Remove-Element
Given an integer array nums and an integer val, remove all occurrences of val in nums in-place. The order of the elements may be changed. Then return the number of elements in nums which are not equal to val.  Consider the number of elements in nums which are not equal to val be k, to get accepted, you need to do the following things.


class Solution:
    def removeElement(self, nums, val):
        if not nums:
            return 0

        slow = 0

        for fast in range(len(nums)):
            if nums[fast] != val:
                nums[slow] = nums[fast]
                slow += 1

        return slow


sol = Solution()

nums1 = [3, 2, 2, 3]
val1 = 3
k1 = sol.removeElement(nums1, val1)
print(k1, nums1)  

nums2 = [0, 1, 2, 2, 3, 0, 4, 2]
val2 = 2
k2 = sol.removeElement(nums2, val2)
print(k2, nums2)  
