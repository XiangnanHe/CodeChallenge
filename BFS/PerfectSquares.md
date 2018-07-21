Given a positive integer n, find the least number of perfect square numbers (for example, 1, 4, 9, 16, ...) which sum to n.

Example 1:

Input: n = 12
Output: 3 
Explanation: 12 = 4 + 4 + 4.
Example 2:

Input: n = 13
Output: 2
Explanation: 13 = 4 + 9.


C++:

class Solution {
public:
    int numSquares(int n) {
        int i = 1;
        int res = 0;
        vector<int> list;
        list.push_back(n);
        return helper(list, res);
    }
    int helper( vector<int> &list, int res){        
        vector<int> nextList;
        for(size_t i = 0; i< list.size(); i++){
            int j = 1;
            int temp = list[i];            
            while(j*j <= temp){
                if(j*j == temp){
                    return res+1;
                }
                nextList.push_back(temp - j*j);
                j++;
            }
        }
        return helper(nextList, res + 1);
        
    }
};
