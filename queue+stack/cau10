stack<int> stac;
void rev(string& s, int start, int end);
string pararev(string &s, int i);
string parenthesesReversal(string s) {
    // STUDENT ANSWER
    return pararev(s, 0);
}
//void rev(string &s,int start,int end);
string pararev(string &s, int i) {
    //cout << i << endl;
    //cout << s[i] << endl;
    //cout << stac.size()<<endl;
    if (s[i] == '\0') {
        return s;
    }
    if (s[i] == '(') {
        //cout << "not ok" << endl;
        stac.push(i);
        s.erase(i, 1);
        return pararev(s, i);
    }
    else if (s[i] == ')') {
        rev(s, stac.top(), i - 1);
        s.erase(i, 1);
        stac.pop();
        return pararev(s, i);
    }
    return pararev(s, i + 1);
}
void rev(string& s, int start, int end) {
    for (int i = start, j = end; i < j; i++, j--) {
        char temp = s[i];
        s[i] = s[j];
        s[j] = temp;
    }

}