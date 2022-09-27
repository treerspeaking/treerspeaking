LLNode* addLinkedList(LLNode* l0, LLNode* l1) {
    // STUDENT ANSWER
    if(l0==nullptr&&l1==nullptr){
        return nullptr;
    }
    LLNode *ret=new LLNode;
    LLNode *start= ret;
    int nho=0;
    while(l0!=nullptr&&l1!=nullptr){
        //ret->next=new LLNode();
        //ret=ret->next;
        if(l0->val+l1->val+nho>=10){
            ret->val=(l0->val+l1->val+nho)%10;
            nho=1;
        }
        else{
            ret->val=(l0->val+l1->val+nho)%10;
            nho=0;
        }
        l0=l0->next;
        l1=l1->next;
        if(l0!=nullptr&&l1!=nullptr){
        ret->next=new LLNode();
        ret=ret->next;
        }
    }
    while(l1!=nullptr){
        ret->next=new LLNode();
        ret=ret->next;
        ret->val=l1->val+nho;
        l1=l1->next;
        nho=0;
    }
    while(l0!=nullptr){
        ret->next=new LLNode();
        ret=ret->next;
        ret->val=l0->val+nho;
        l0=l0->next;
        nho=0;
    }
        //cout<<nho<<endl;
    if(nho){
        ret->next=new LLNode();
        ret=ret->next;
        ret->val=nho;
    }
    //cout<<total<<endl;
    
    return start;
}