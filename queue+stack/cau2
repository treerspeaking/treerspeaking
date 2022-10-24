// iostream, vector and queue are included
// You can write helper methods

long long nthNiceNumber(int n) {
    queue<long long> q;
    q.push(2);
    q.push(5);
    for(int i=1;i<n;i++){
        long long temp=q.front();
        q.pop();
        q.push(temp*10+2);
        q.push(temp*10+5);
    }
    return q.front();
}