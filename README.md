# BCZY7
第七次编程作业
关于力扣的一些刷题
两数之和：
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
删除有序数组中的重复项:
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
