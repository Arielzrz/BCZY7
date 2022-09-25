# BCZY7
第七次编程作业
关于力扣的一些刷题
1.两数之和：
class Solution():
  def twoSum(self,nums, target):
    for i in range(0, len(nums)):
        for j in range(i+1, len(nums)):
            if nums[i]+nums[j] == target:
                return [i,j]
    return []
s=Solution()
nums=[1,2,3,4]
target=3
com=s.twoSum(nums,target)
26.删除有序数组中的重复项:
class Solution(object):
    def removeDuplicates(self, nums):
        if len(nums) == 0:
            return 0
        else:
            j = 1
            for i in range(1, len(nums)):
 
                if nums[i-1] != nums[i]:
                    nums[j] = nums[i]
                    j +=1
            return j
27.移除元素：
class Solution(object):
    def removeElement(self, nums, val):
        n=len(nums)
        j=0
        for i in range(n):
            if nums[i]!=val:
                nums[j]=nums[i]
                j=j+1
            else:
                continue
        return j
35.搜索插入位置：
class Solution(object):
    def searchInsert(self,nums, target):
        n=len(nums)
        if target in nums:
            for i in range(n):
                if nums[i]==target:
                    return i
        else:
            for i in range(n):
                if target<nums[i]:
                    return i
 66.加一：
 class Solution(object):
    def plusOne(self, digits):
        n=len(digits)
        digits[n-1]+=1
        return digits
