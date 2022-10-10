template <class T>
T DLinkedList<T>::removeAt(int index)
{
    Node* temp = head;
    /* Remove element at index and return removed value */
    if(temp==nullptr){return 0;}
    T ret;
    if(index==0){
        Node*hold=head->next;
        if(head==tail){
            tail=nullptr;
        }
        ret=head->data;
        delete head;
        head=hold;
        if(head!=nullptr)
        head->previous=nullptr;
        //return ret;
    }
    else if(index==count-1){
        Node*hold=tail->previous;
        ret = tail->data;
        delete tail;
        tail=hold;
        tail->next=nullptr;
        //return ret;
    }
    else{
        Node*dummy_head=head;
        for(int i=0;i<index;i++){
            dummy_head=dummy_head->next;
        }
        Node*temp_prev = dummy_head->previous;
        Node*temp_next =  dummy_head->next;
        ret= dummy_head->data;
        delete dummy_head;
        temp_prev->next=temp_next;
        temp_next->previous=temp_prev;
    }
    //T a = temp->data;
    //delete temp;
    count--;
    return ret;
}

template <class T>
bool DLinkedList<T>::removeItem(const T& item)
{
    /* Remove the first apperance of item in list and return true, otherwise return false */
    Node* temp = head;
    for (int i = 0; temp != nullptr; i++) {
        if (temp->data == item) {
            removeAt(i);
            return true;
        }
        temp = temp->next;
    }
    return false;

}

template<class T>
void DLinkedList<T>::clear() {
    /* Remove all elements in list */
    Node* temp = head;
    while (temp != nullptr) {
        //cout << temp->data << endl;
        Node* next = temp->next;
        delete temp;
        temp = next;
    }
    head = nullptr;
    tail = nullptr;
    count = 0;
}