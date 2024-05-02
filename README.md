//# find-k-closest-element
class Solution {
public:
vector<int>twopointermethod(vector<int>& arr, int k, int x){
      int high=arr.size()-1;
        int low=0;
        while(high-low>=k){
            if(x-arr[low]>arr[high]-x){
                low++;
            }
            else{
                high--;
            }
        }
        vector<int>ans;
for(int i=low;i<=high;i++){
    ans.push_back(arr[i]);
}
return ans;
}
    vector<int> findClosestElements(vector<int>& arr, int k, int x) {
      return twopointermethod(arr,k,x);
    }
};
