class Solution {
public:
    ListNode* deleteDuplicates(ListNode* head) {
        if(head==nullptr)
        return nullptr;
        ListNode*curr=head;
        while(curr!=nullptr&&curr->next!=nullptr){
          if(curr->val==curr->next->val){    // duplicate node mila, skip kar do
        curr->next=curr->next->next;
        }
        else{
        curr=curr->next;
    }
        }
    return head;
    }
};

<img width="1884" height="815" alt="image" src="https://github.com/user-attachments/assets/f7f7a5c4-f78d-47bf-9f06-31c71c21d955" />
