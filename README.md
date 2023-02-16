class Solution {
    public int findDuplicate(int[] nums) {
        /*
        Arrays.sort(nums);//12234
        for(int i=0;i<nums.length-1;i++)
        {
            if(nums[i]==nums[i+1])//2==2
            {
               return nums[i];//2
            }

        }
        return -1;
        */
        HashSet<Integer>set=new HashSet<>();
        for(int i:nums)
        {
            if(set.contains(i))
            {
                return i;
            }
            set.add(i);//2
        }
        return -1;
    }
}
