long int midSquare(long int seed)
{
    long long square=seed*seed;
    square/=100;
    return square%10000;
    
    
}
long int moduloDivision(long int seed, long int mod)
{
    return seed%mod;
}
long int digitExtraction(long int seed,int* extractDigits,int size)
{
    int b=1;
    while(seed/b!=0){
        b*=10;
    }
    b/=10;
    int count=0;
    long int sum=0;
    for(int i=0;seed!=0;i++){
        int du=seed/b;
        //cout<<du<<endl;
        if(extractDigits[count]==i){
            sum=sum*10+du;
            count++;
        }
        seed=seed-du*b;
        b/=10;
    }
    return sum;
}