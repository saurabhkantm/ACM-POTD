class Solution {
public:
    ListNode* reverseList(ListNode* head) {
        // Base case: empty list or single node
        if (head == nullptr || head->next == nullptr) {
            return head;
        }

        // Reverse the rest of the list
        ListNode* last = reverseList(head->next);

        // Put current node at the end
        head->next->next = head;
        head->next = nullptr;

        return last;
    }
};
<img width="1905" height="862" alt="image" src="https://github.com/user-attachments/assets/0595ebf6-728e-48c6-b224-c3da5a834494" />
