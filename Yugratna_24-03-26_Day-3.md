Q. You are given an array prices where prices[i] is the price of a given stock on the ith day.  

You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.  

Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.  

Ans:  

class Solution {  
public:  
    int maxProfit(vector<int>& prices) {  
       int mini= prices[0];  
       int maxProfit=0;  
       int n= prices.size();  
       for(int i=1; i<n; i++){  
        int cost= prices[i]-mini;  
        maxProfit= max(maxProfit,cost);  
        mini= min(mini, prices[i]);  
       }  
       return maxProfit;  
    }  
};  

<img width="1449" height="740" alt="image" src="https://github.com/user-attachments/assets/a663ddcc-700e-49b0-859e-460ba1b9c38b" />


