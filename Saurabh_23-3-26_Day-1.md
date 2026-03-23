class Solution {
public:
    int firstMissingPositive(vector<int>& nums) {
        int n=nums.size();
        for (int i = 0; i < n; i++) {
            while (nums[i] > 0 && nums[i] <= n && nums[nums[i]-1] != nums[i]) {
                swap(nums[i], nums[nums[i]-1]);
            }
        }
        for (int i = 0; i < n; i++) {
            if (nums[i] != i + 1)
                return i + 1;
        }
        
        return n + 1;
    }
};
<img width="1890" height="863" alt="image" src="https://github.com/user-attachments/assets/35e94642-3c25-48b9-96a1-5dbc2f9ad8fb" />
