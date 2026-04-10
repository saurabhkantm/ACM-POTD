class Solution {
public:
    string makeGood(string s) {
       string st;
    for (char c : s) {
        if (!st.empty()&&abs(st.back()-c)==32) st.pop_back();
        else st+=c;
    }
    return st; 
    }
};
<img width="1883" height="848" alt="image" src="https://github.com/user-attachments/assets/10ac0171-d978-4fb5-ac8d-756b79665a85" />
