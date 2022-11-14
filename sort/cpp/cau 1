template <class T>
void SLinkedList<T>::bubbleSort()
{
    Node*tailtemp=tail;
    Node*prev=nullptr;
    Node*dummy=head;
    while(dummy!=tailtemp){
        while(dummy!=tailtemp){
            if(dummy->data>dummy->next->data){
                int temp=dummy->data;
                dummy->data=dummy->next->data;
                dummy->next->data=temp;
            }
            prev=dummy;
            dummy=dummy->next;
        }
        //headtemp=headtemp->next;
        tailtemp=prev;
        dummy=head;
        printList();
    }
}