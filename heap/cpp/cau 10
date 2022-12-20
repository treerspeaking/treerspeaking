int uglyNumberIndex(int n) {
    // STUDENT ANSWER
    priority_queue<int,vector<int>,greater<int>> pq;
    int prime[]={2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31 };
    for(int i=0;i<11;i++){
        pq.push(prime[i]);
    }
    int temp=1;
    for(int i=0;i<n;i++){
        temp=pq.top();
        //cout<<temp<<endl;
        pq.pop();
        for(unsigned int j=0;j<sizeof(prime)/sizeof(int);j++){
            pq.push(prime[j]*temp);
        }
        int top=pq.top();
        pq.pop();
        while(top==pq.top()){
            pq.pop();
        }
        pq.push(top);
    }
    return temp;
}