template <class T>
void DLinkedList<T>::add(const T& e) {
    if (count == 0)
    {
    Node* newNode = new Node(e);
    head = newNode;
    tail = newNode;
    tail->next = NULL;
    ++(this->count);
    return;
    }
    Node* newNode = new Node(e);
    tail->next = newNode;
    newNode->previous = tail;
    newNode->next = NULL;
    tail = newNode;
    ++(this->count);
    return;
}

template<class T>
void DLinkedList<T>::add(int index, const T& e) {
    /* Insert an element into the list at given index. */
if (count == 0) {add(e);return;}
if (index == 0)
{
Node* newNode = new Node(e);
newNode->next = head;
head->previous = newNode;
head = newNode;
++(this->count);
return;
}
    if (index == this->count) {add(e); return;}
    int idx = 0;
    Node* front = head;
    Node* back = NULL;
    for (;front != NULL; back = front, front = front->next, ++idx)
    {
        if (idx == index)
        {
        Node* newNode = new Node (e);
        ++(this->count);
        back->next = newNode;
        newNode->next = front;
        front->previous = newNode;
        return;
        }
    }
    
}

template<class T>
int DLinkedList<T>::size() {
    /* Return the length (size) of list */ 
    int cnt=0;
    Node*temp=head;
    while(temp!=nullptr){
        temp=temp->next;
        cnt++;
    }
    return cnt;
}