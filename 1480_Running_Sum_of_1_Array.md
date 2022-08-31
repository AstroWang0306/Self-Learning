Description:

Given an array nums. We define a running sum of an array as runningSum[i] = sum(nums[0]…nums[i]).

Return the running sum of nums.

Ex: Given an array: nums[1,2,3,4,5], the output will be a int array which contains: output[nums[0], nums[0]+nums[1]...,nums[0]+..+nums[4]]

Hence, the output will be [1,3,6,10,15]

Solution:

    public int[] runningSum(int[] nums) {
    
        int sum[] = new int[nums.length];
        
        int total = 0;
        
        for (int i = 0; i<nums.length; i++) {
        
            total += nums[i];
            
            sum[i] = total;
            
        }
        
        return sum;
        
    }
    

Use Iteration and create another array to store the sum of each elements. 

