# GFG 16-Days Problem Solving Challenge

## 📅 Day 7: Buy and Sell Stock

### 🚀 Problem Statement
You are given an array `prices[]` where `prices[i]` represents the stock price on the `i-th` day. Your task is to determine the **maximum profit** that can be earned by buying and selling stocks multiple times.

**Note:** You may complete as many transactions as needed (buy one and sell one share multiple times), but you **must sell the stock before buying again**.

### 🔹 Example
#### Input:
```plaintext
prices = [7,1,5,3,6,4]
```
#### Output:
```plaintext
7
```
#### Explanation:
- Buy on day 2 (price = 1) and sell on day 3 (price = 5), profit = 5 - 1 = 4.
- Buy on day 4 (price = 3) and sell on day 5 (price = 6), profit = 6 - 3 = 3.
- Total profit = 4 + 3 = 7.

---

## 🛠 Approach
- Iterate through the `prices` array from day 1 to the last day.
- Whenever the price of a stock on a given day is **higher than the previous day**, add the profit.
- This ensures that **every profitable trade** is accounted for.

### 📝 Code Implementation
#### Java Solution ☕
```java
class Solution {
    public int maximumProfit(int prices[]) {
        int profit=0;
        for(int i=1;i<prices.length;i++){
            if(prices[i]>prices[i-1]){
                profit+=prices[i]-prices[i-1];
            }
        }
        return profit;
    }
}
```

---

## ⏳ Complexity Analysis
- **Time Complexity**: O(n) → Single pass through the array.
- **Space Complexity**: O(1) → Constant space used.

---

## 🔗 Related Links
- [GeeksforGeeks Problem Link](https://www.geeksforgeeks.org/) *(Replace with the actual problem link)*
- [Java Arrays Documentation](https://docs.oracle.com/javase/8/docs/api/java/util/Arrays.html)

---

## ⭐ Like this repository?
Give it a ⭐ if you found this helpful!
