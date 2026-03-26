class Solution {
public:
    vector<int> productExceptSelf(vector<int>& nums) {
        int n=nums.size();
        vector<int>ans(n,1);
        int left=1;
        for(int i=0;i<nums.size();i++){
            ans[i]*=left;
            left*=nums[i];
        }
        int r=1;
        for(int i=nums.size()-1;i>=0;i--){
            ans[i]*=r;
            r*=nums[i];
        } 
        return ans;  
    }
};
<img width="1903" height="857" alt="image" src="https://github.com/user-attachments/assets/9d037e92-7252-4f74-9af7-7e4510577982" />
