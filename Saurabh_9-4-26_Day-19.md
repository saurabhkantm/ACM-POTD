class Solution {
private:
    int getNextValidChar(string& s, int index) {
        int backspace = 0;
        while (index >= 0) {
            if (s[index] == '#') {
                backspace++;
            } else if (backspace > 0) {
                backspace--;
            } else {
                break;
            }
            index--;
        }
        return index;
    }
    
public:
    bool backspaceCompare(string s, string t) {
        int i = s.length() - 1, j = t.length() - 1;
        
        while (i >= 0 || j >= 0) {
            i = getNextValidChar(s, i);
            j = getNextValidChar(t, j);
            
            if (i >= 0 && j >= 0 && s[i] != t[j]) {
                return false;
            }
            if ((i >= 0) != (j >= 0)) {
                return false;
            }
            i--;
            j--;
        }
        return true;
    }
};
<img width="1904" height="858" alt="image" src="https://github.com/user-attachments/assets/2a759339-26b1-4860-8837-4f21a6d2eebd" />
