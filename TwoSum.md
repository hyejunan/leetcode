### 1. Two Sum

***Easy***</br>

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

```Java
// Java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int[] arr = new int[2];
        for(int i=0;i<nums.length;i++) {
            int num = target - nums[i];
            for(int j=i+1;j<nums.length;j++) {
                if (nums[j] == num) {
                    arr[0] = i;
                    arr[1] = j;
                    return arr;
                }
            }
        }
        return arr;
    }
}
````
```C++
// C++
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
       vector<int> arr;
       for(auto i=0;i<nums.size();i++) {
           auto num = target - nums.at(i);
           for(auto j=i+1;j<nums.size();j++) {
               if(nums.at(j) == num) {
                   arr.push_back(i);
                   arr.push_back(j);
                   return arr;
               }
           }
       }
        return arr;
    }
};
```
````JavaScript
//JavaScript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    var num=-1;
    arr = [];
    for(var i=0;i<nums.length;i++) {
        num = target - nums[i];
        for(var j=i+1;j<nums.length;j++) {
            if(num==nums[j]) {
                arr = [i,j];
                return arr;
            }
        }
    }
};
```



