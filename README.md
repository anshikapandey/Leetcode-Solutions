# Leetcode-Solutions
class Solution:
    def findMaxAverage(self, nums,k):
        max_avg=sum(nums[0:k])
        test=sum(nums[0:k])
        for i in range(1,len(nums)-k+1):            
          test=test-nums[i-1]+nums[i+k-1]        
          max_avg=max(max_avg,test)
        return max_avg/k
