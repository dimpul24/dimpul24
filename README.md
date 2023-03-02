//KTH-LARGEST ELEMENT USING HEAP
#include <iostream>
#include<bits/stdc++.h>
using namespace std;
int findkthLargest(vector<int>& nums, int k) {
	priority_queue<int,vector<int>,greater<int>> pq;
	for(int i=0;i<nums.size();++i){
		pq.push(nums[i]);
		if(pq.size()>k) pq.pop();
	}
	return pq.top();            
}

int main()
{
    vector<int> nums={3,2,1,5,6,4};
    int k=3;
    cout<<findkthLargest(nums,k);

    return 0;
}
