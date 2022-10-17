template<class T>
T DLinkedList<T>::get(int index) {
    if (count == 0) return -1;
    if (index == this->count - 1) return tail->data;
    if (index == 0) return head->data;
    int idx = 0;
    for (Node* h = head; h != NULL; h = h->next, ++idx)
    {
        if (idx == index) return h->data;
    }
return -1;
/* Give the data of the element at given index in the list. */
}
template <class T>
void DLinkedList<T>::set(int index, const T& e) {
    if (count == 0) return;
    if (index == 0)
    {
        head->data = e;
    return;
    }
    if (index == this->count - 1)
    {
        tail->data = e;
        return;
    }
    int idx = 0;
    for (Node* h = head; h != NULL; h = h->next, ++idx)
    {
        if (idx == index)
        {
            h->data = e;
            return;
        }
    }
/* Assign new value for element at given index in the list */
}

template<class T>
bool DLinkedList<T>::empty() {
/* Check if the list is empty or not. */
    if (count ==0) return true;
    return false;
    
}

template<class T>
int DLinkedList<T>::indexOf(const T& item) {
    /* Return the first index wheter item appears in list, otherwise return -1 */
    int idx=0;
    if(count==0) return -1;
    for(Node*temp_head=head;temp_head!=nullptr;temp_head=temp_head->next,idx++){
        if(item==temp_head->data){
            return idx;
        }
    }
    return -1;
    
}

template<class T>
bool DLinkedList<T>::contains(const T& item) {
    /* Check if item appears in the list */
    Node*temp=head;
    while(temp!=nullptr){
        if(temp->data==item){
            return 1;
        }
        temp=temp->next;
    }
    return 0;
    
}