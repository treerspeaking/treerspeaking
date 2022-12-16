template<class T>
int Heap<T>::getItem(T item) {
    // TODO: return the index of item in heap
    for(int i=0; i<count; i++) {
        if(elements[i] == item) return i;
    }
    return -1;
}

template<class T>
void Heap<T>::remove(T item) {
    // TODO: remove the element with value equal to item
    int index = getItem(item);
    elements[index] = elements[--count];
    reheapUp(index);
    reheapDown(index);
}

template<class T>
void Heap<T>::clear() {
    // TODO: delete all elements in heap
    count = 0;
}