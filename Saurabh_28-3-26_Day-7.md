class Solution {
public:
    void reverse(vector<int>&nums,int start,int end){
        while(start<=end){
            swap(nums[start],nums[end]);
            start++;
            end--;
        }
        return;
    }
    void rotate(vector<int>& nums, int k) {
        int n = nums.size();
        k = k%n;
        reverse(nums,0,n-k-1);
        reverse(nums,n-k,n-1);
        reverse(nums,0,n-1);
        return;
    }
};


<img width="1880" height="857" alt="image" src="https://github.com/user-attachments/assets/961538c4-546c-47bd-b4c2-f0646a3140ce" />
