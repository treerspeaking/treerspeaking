int sumOfMaxSubarray(vector<int>& nums, int k) {
    deque<int> d; // deque to store INDICES of Maximums (usually in the front of deque)

    // deque elements would be arranged:
    // Max --- Min

    int sum = 0;

    // Push in maximum of the first subarray
    int i = 0;
    while (i < k)
    {
        while (!d.empty() && nums.at(i) >= nums.at(d.back()))
            d.pop_back();
        
        d.push_back(i);
        ++i;
    }
    sum += nums.at(d.front()); // Front is always a maximum value of the current subarray

    // Continue with other elements
    // nums[i] is new element added
    while (i < (int)nums.size())
    {
        // Pop old elements
        if (!d.empty() && d.front() < i - k + 1)
            d.pop_front();
        
        while (!d.empty() && nums.at(i) >= nums.at(d.back()))
            d.pop_back();
        
        d.push_back(i);
        ++i;

        sum += nums.at(d.front());
    }

    return sum;
}