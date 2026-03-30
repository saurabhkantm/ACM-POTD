class Solution {
public:
    ListNode* middleNode(ListNode* head) {
        ListNode*slow=head;
        ListNode*fast=head;
        //fast do step chale ga aur slow ek step
        while(fast!=nullptr&&fast->next!=nullptr){
        slow=slow->next;
        fast=fast->next->next;
    }
    return slow;
    }
};

<img width="1872" height="851" alt="image" src="https://github.com/user-attachments/assets/467b04f5-5b3f-493c-9fe6-0b2392d91258" />
