class Solution {
public:
    int hammingDistance(int x, int y) {
        int j=0;
    vector<int>v1;
    vector<int>v2;
   while(x>0||y>0)
    {
       v1.push_back(x%2);
       v2.push_back(y%2);
       x=x/2;
       y=y/2;
    }

  // for(int i:v1)
  //   cout<<i;
  //   cout<<endl;
  //   for(int i:v2)
  //       cout<<i;
    for(int i=0;i<v1.size();i++)
    {
        if(v1[i]!=v2[i])
        {
            j++;
        }
    }
        return j;
    }
};
