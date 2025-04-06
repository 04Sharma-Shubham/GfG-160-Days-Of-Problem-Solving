# 🧠 GFG 160 Days Problem Solving Challenge

Welcome to the **GFG 160 Days Problem Solving Challenge** repository! This repo contains daily solutions to problems from the challenge, written in Java. Each solution is optimized and explained for better understanding and preparation.

---

## 📅 Day 10 - Kadane's Algorithm

### 🔸 Problem Statement

Given an array of integers, the task is to find the contiguous subarray (containing at least one number) which has the largest sum and return its sum.

---

### 💡 Example

**Input:**
```
arr = [-2,1,-3,4,-1,2,1,-5,4]
```


**Output:**
```
6
```

**Explanation:**  
The subarray `[4, -1, 2, 1]` has the maximum sum `6`.

---

### ✅ Solution

```java
class Solution {
    public int maximumSumSubarray(int[] arr, int n){
        int maxSoFar = arr[0];
        int currMax = arr[0];
        
        for (int i = 1; i < n; i++) {
            currMax = Math.max(arr[i], currMax + arr[i]);
            maxSoFar = Math.max(maxSoFar, currMax);
        }
        
        return maxSoFar;
    }
}
```
🔍 Approach
Use Kadane’s Algorithm, which maintains a running current sum and updates the maximum found so far.

If the current sum becomes less than the current element, restart the subarray from the current element.

⏱️ Time Complexity
O(n) – Single pass through the array.

📁 Repository Structure
```
📂 GFG-160Days-Solutions/
  ┣ 📄 README.md
  ┗ 📁 Day10_KadanesAlgorithm/
     ┗ 📄 Solution.java
```
⭐️ Keep Solving & Keep Growing!
Don't forget to star 🌟 the repo if you find it helpful! Contributions and feedback are welcome.


Let me know if you’d like me to generate the actual `.md` file 
