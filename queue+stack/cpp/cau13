int sumOfMinSubarray(vector<int>& a) {
    // STUDENT ANSWER
    int mod = 10000;
    stack<int>st;
    int n = a.size();
    int dp[n];
    for (int  i =0; i<n; i++)
    {
        while (!st.empty()&&a[st.top()]>=a[i])
        {
            st.pop();
        }
        if (!st.empty())
        {
            int pre = st.top();
            dp[i] = dp[pre]+(i-pre)*a[i];
        }
        else {
                // or it doesn't exist, in this case the current element
                // contributes with all subarrays ending at i
            dp[i] = (i + 1) * a[i];
        }
            // push the current index
        st.push(i);
    }
    int res = 0;
    for (int i =0; i<n; i++)
    {
        res+=dp[i];
        res%=mod;
    }
    return res;
}