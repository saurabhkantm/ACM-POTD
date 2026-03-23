class Solution {
public:
    void sortColors(vector<int>& nums) {
        int n = nums.size();
        int i = 0 ; //0 
        int j = 0; //1
        int k = n-1; //2
        while(j <= k){
            if(nums[j] == 1) j++;
            else if(nums[j] == 2){
                swap(nums[j],nums[k]);
                k--;
            }else{
                swap(nums[j],nums[i]);
                i++;
                j++;
            }
        }
    }
};
<img width="1883" height="865" alt="Screenshot 2026-03-24 011901" src="https://github.com/user-attachments/assets/4626c9b0-7557-4073-bd80-872210738c7d" />
