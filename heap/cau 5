//Helping functions go here
static void heapSort(T* start, T* end){
    //TODO
    priority_queue<int,vector<int>,greater<int>> pq;
    for(int i=0;i<end-start;i++){
        pq.push(start[i]);
    }
    for(int i=0;i<end-start;i++){
        start[i]=pq.top();
        pq.pop();
    }
    Sorting<T>::printArray(start,end);
}