int mountainWithoutValley(vector<int>& nums) {
    // STUDENT ANSWER
    vector<pair<int,int>> up;
    vector<pair<int,int>> down;
    int max=INT_MIN;
    up.push_back({nums[0],0});
    //down.push_back({nums[0],0});
    int size=nums.size();
    int sum1=nums[0];
    for(int i=1;i<size;i++){
        pair<int,int> temp_up_back=up.back();
        if(nums[i]>=temp_up_back.first){
            up.push_back({nums[i],i});
            sum1+=nums[i];
        }
        else {
            int sum2;
            if(nums[i]*(size-i-1)+sum1<=max){
                goto skip;
            }
            down.push_back({nums[i],i});
            sum2=nums[i];
            for(int j=i+1;j<size;j++){
                pair<int,int> temp_down_back=down.back();
                if(nums[j]<=temp_down_back.first){
                    if(sum1+sum2+nums[j]*(size-j-1)<max)  {down.clear();goto skip;}
                    down.push_back({nums[j],j});
                    sum2+=nums[j];
                }
                else{
                    //temp_down_back.second++;
                    down[down.size()-1].second++;
                    sum2+=down[down.size()-1].first;
                }
            }
            if(sum1+sum2>max){
                max=sum1+sum2;
            }
            down.clear();
            skip:
            while(nums[i]<temp_up_back.first){
                if(up.size()==1){sum1-=up[0].first*(up[0].second+1);}
                else {
                    int up_size=up.size();
                    sum1 -= up[up_size-1].first*(up[up_size-1].second-up[up_size-2].second);
                    
                }
                //sum1-=temp_up_back.first;
                up.pop_back();
                if(up.size()==0){
                    break;
                }
                temp_up_back=up.back();
            }
            up.push_back({nums[i],i});
            if(up.size()==1)
            sum1+=nums[i]*(i-0+1);
            else
            sum1+=nums[i]*(up[up.size()-1].second-up[up.size()-2].second);
        }
    }
    sum1=up[0].first*(up[0].second+1);
            int up_size=up.size();//add phần up
            for(int j=1;j<up_size;j++){
                sum1=sum1+up[j].first*(up[j].second-up[j-1].second);
            }
            //cout<<"sum1_up"<<sum1<<endl;
            if(sum1>max) max=sum1;
    return max;
}