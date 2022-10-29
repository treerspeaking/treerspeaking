bool tripleIndexSLM(vector<int>& nums) {
    // STUDENT ANSWER
    if(nums.size()<=2){
        return 0;
    }
    vector<int> v;
    v.resize(2);
    deque<int> de;
    if(nums[0]<=nums[1]){
        v[0]=nums[0];
        v[1]=nums[1];
    }
    else{
        v[0]=nums[1];
        v[1]=nums[0];
    }
    for(unsigned int i=2;i<nums.size();i++){
        if(v[0]<nums[i]&&nums[i]<v[1]){
            return true;
        }
        if(nums[i]<=v[0]){
            de.push_front(nums[i]);
        }
        else if(v[1]<=nums[i]){
            de.push_back(nums[i]);
        }
        if(de.size()==2){
            v[0]=de[0];
            v[1]=de[1];
            de.clear();
        }
    }
    return false;
}