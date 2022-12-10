int foldShift(long long key, int addressSize)
{
    long long b=1;
    while((key/b)!=0){
        b=b*10;
    }
    int fold=0;
    while(key!=0){
        for(int i=0;i<addressSize;i++){
            b/=10;
            if(b==1) break;
        }
        int split=key/b;
        key-=split*b;
        fold+=split;
    }
    int c=1;
    for(int i=0;i<addressSize;i++){
        c=c*10;
    }
    return fold%c;
}

int rotation(long long key, int addressSize)
{
    long long b=1;
    while(key/b!=0){
        b=b*10;
    }
    b/=10;
    int du=key%10;
    key/=10;
    key=du*b+key;
    //cout<<key<<endl;
    return foldShift(key,addressSize);
}