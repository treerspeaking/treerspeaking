template <class T>
void Sorting<T>::selectionSort(T *start, T *end)
{
    for(int i=0;i<end-start-1;i++){
        int min=i;
        for(int j=i+1;j<end-start;j++){
            if(start[j]<start[min]){
                min=j;
            }
        }
        swap(start[i],start[min]);
        printArray(start, end);
    }
}