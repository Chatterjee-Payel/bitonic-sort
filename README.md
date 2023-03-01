# bitonic-sort
	
	
	public:
	  
	void bitonicGenerator(int arr[], int n)
	{
		// Your code goes here
	vector<int>v1;
	vector<int>v2;
	for(int i=0;i<n;i+=2)
	{
	    v1.push_back(arr[i]);
	}
	sort(v1.begin(),v1.end());
	for(int i=1;i<n;i+=2)
	{
	    v2.push_back(arr[i]);
	    
	}
	sort(v2.begin(),v2.end());
	reverse(v2.begin(),v2.end());
	vector<int>v3(v1);
	v3.insert(v3.end(),v2.begin(),v2.end());
	for(int i=0;i<n;i++){
	    arr[i]=v3[i];
	}
	}
};
