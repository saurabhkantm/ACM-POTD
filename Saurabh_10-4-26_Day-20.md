class Solution {
public:
    string removeKdigits(string num, int k) {
        string stk;
        for (char& c : num) {
            while (k && stk.size() && stk.back() > c) {
                stk.pop_back();
                k--;
            }
            stk += c;
        }
        while (k--) {
            stk.pop_back();
        }
        int i = 0;
        for (; i < stk.size() && stk[i] == '0'; ++i) {
        }
        string ans = stk.substr(i);
        return ans == "" ? "0" : ans;
    }
};
<img width="1866" height="862" alt="image" src="https://github.com/user-attachments/assets/17eb8951-110e-4de4-8153-228608a32a79" />
