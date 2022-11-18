// You must use the nodes in the original list and must not modify ListNode's val attribute. 
// Hint: You should complete the function mergeLists first and validate it using our first testcase example

// Merge two sorted lists
ListNode* mergeLists(ListNode* a, ListNode* b) {
    ListNode*result=nullptr;
    if(a==nullptr) return (b);
    if(b==nullptr) return (a);
    if(a->val<=b->val){
        result=a;
        result->next=mergeLists(a->next,b);
    }
    else{
        result=b;
        result->next=mergeLists(a,b->next);
    }
    return result;
}

// Sort and unsorted list given its head pointer
void split(ListNode*source,ListNode*&front,ListNode*&back){
    ListNode* slow=source;
    ListNode*fast =source->next;
    while(fast!=nullptr){
        fast=fast->next;
        if(fast!=nullptr){
            slow=slow->next;
            fast=fast->next;
        }
    }
    front=source;
    back=slow->next;
    //cout<<back->val<<endl;
    slow->next=nullptr;
}
ListNode* mergeSortList(ListNode* head) {
    if(head==nullptr||head->next==nullptr) return head;
    //cout<<head->val<<endl;
    //cout<<head->next->val<<endl;
    ListNode*a;
    ListNode*b;
    split(head,a,b);
    a=mergeSortList(a);
    b=mergeSortList(b);
    head=mergeLists(a,b);
    return head;
}