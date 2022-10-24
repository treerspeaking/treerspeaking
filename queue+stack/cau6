int baseballScore(string ops){
/*TODO*/
    vector<int> v;
    int size=ops.size();
    for(int i=0;i<size;i++){
        //cout<<ops[i]<<endl;
        if('0'<=ops[i]&&ops[i]<='9'){
            v.push_back(ops[i]-48);
            //cout<<ops[i]<<endl;
        }
        else if(ops[i]=='C'){
            v.pop_back();
        }
        else if(ops[i]=='D'){
            int temp=v.back();
            //cout<<v.back()<<endl;
            v.push_back(temp*2);
        }
        else if(ops[i]=='+'){
            int temp=v.back();
            vector<int>::iterator temp_back=v.end();
            temp_back--;
            temp_back--;
            int temp2=*temp_back;
            v.push_back(temp+temp2);
        }
        //cout<<v[0]<<endl;
    }
    int sum=0;
    for(unsigned int i=0;i<v.size();i++){
        sum+= v[i];
    }
    return sum;
}