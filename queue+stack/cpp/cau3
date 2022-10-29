// iostream and queue are included
// Hint: Use a queue to simulate the process

int numberOfTheWinner(int N, int k) {
    queue<int> q;
    for(int i=1;i<=N;i++){
        q.push(i);
    }
    while(q.front()!=q.back()){
        int x=k-1;
        while(x>0){
            int temp=q.front();
            q.pop();
            q.push(temp);
            x--;
        }
        q.pop();
    }
    return q.front();
}