GeeksforGeeks 160 Days of Problem Solving

This repository contains solutions to the GeeksforGeeks 160 Days Problem Solving Challenge, implemented in Java. Each solution is optimized and well-documented for better understanding.

🚀 Day 8: Buy and Sell Stock - Max One Transaction Allowed

Problem Statement:
  
You are given an array prices where prices[i] represents the price of a given stock on the ith day. You are allowed to complete at most one transaction (i.e., buy once and sell once). Find the maximum profit you can achieve. If no profit can be achieved, return 0.

Example:
```
Input: prices = [7,1,5,3,6,4]
Output: 5
Explanation: Buy at price = 1 and sell at price = 6, Profit = 6 - 1 = 5.
```
🔹 Optimized Java Solution
```
class Solution {
    public int maximumProfit(int prices[]) {
        int buyPrice = prices[0], maxProfit = 0;
        for (int i = 0; i < prices.length; i++) {
            if (prices[i] > buyPrice) {
                maxProfit = Math.max(maxProfit, prices[i] - buyPrice);
            } else {
                buyPrice = prices[i];
            }
        }
        return maxProfit;
    }
}
```
📝 Complexity Analysis:

Time Complexity: O(n) (Single pass through the array)

Space Complexity: O(1) (Constant extra space used)

📌 Topics Covered:

Array Manipulation

Greedy Algorithm

Stock Trading Strategies

💡 Additional Notes:

The algorithm tracks the minimum buy price and calculates the profit dynamically.

It ensures optimal profit calculation in linear time without extra space.

⭐ More GFG Solutions

Explore more GeeksforGeeks daily problem-solving solutions in this repository! 🚀

📌 If you find this helpful, don't forget to ⭐ star this repo! 😊

