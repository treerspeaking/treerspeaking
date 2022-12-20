struct mycmp{
    bool operator()(int a,int b){
        return a>b;
    }
};
int leastAfter(vector<int>& nums, int k) {
    // STUDENT ANSWER
    priority_queue<int,vector<int>,mycmp> pq;
    for(unsigned int i=0;i<nums.size();i++){
        pq.push(nums[i]);
    }
    for(int i=0;i<k;i++){
        int temp=pq.top();
        pq.pop();
        pq.push(temp*2);
    }
    return pq.top();
}