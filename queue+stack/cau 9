// iostream, stack and vector are included
vector<int> nextGreater(vector<int>& arr){
    int n=arr.size();
    vector<int>ret;
    ret.resize(arr.size());
    stack<pair<int,int>> s;
    s.push({arr[0],0});
    for(int i=1;i<n;i++){
        pair<int,int> temp=s.top();
        if(temp.first<arr[i]){
            while(temp.first<arr[i]){
                ret[temp.second]=arr[i];
                s.pop();
                if(s.size()==0){
                    goto stop;
                }
                temp=s.top();
            }
            stop:
            s.push({arr[i],i});
        }
        else {
            s.push({arr[i],i});
        }
    }
    int stackn=s.size();
    for(int i=0;i<stackn;i++){
        pair<int,int> temp=s.top();
        ret[temp.second]=-1;
        s.pop();
    }
    return ret;
}