template<class T>
void Heap<T>::push(T item){
    elements[count]=item;
    reheapUp(count);
    count++;
    if(count>=capacity) ensureCapacity(count*2);
}

template<class T>
void Heap<T>::ensureCapacity(int minCapacity){
    T* newele=new T[minCapacity];
    for(int i=0;i<capacity;i++){
        newele[i]=elements[i];
    }
    delete []elements;
    elements=newele;
    capacity= minCapacity;
}

template<class T>
void Heap<T>::reheapUp(int position){
    while(position!=0){
        int par=(position-1)/2;
        if(elements[par]<elements[position]){
            swap(elements[par],elements[position]);
            position=par;
        }
        else break;
    }
}