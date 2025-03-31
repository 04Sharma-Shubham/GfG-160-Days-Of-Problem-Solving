# 🚀 GFG 160 Days of DSA Challenge

Welcome to my **GeeksforGeeks 160 Days Problem Solving** journey!  
This repository contains **well-structured Java solutions** for each day's problem, including explanations and complexity analysis.

---

## 📌 Features

- ✅ **160 Days of GFG Problems**
- 🧪 **Optimized Java solutions**
- 📂 **Structured by Day**
- 📊 **Time & Space Complexity Analysis**
- 📝 **Beginner-friendly & Interview-focused**

---

## 📅 Progress Tracker

| Day  | Problem | Difficulty | Solution |
|------|---------|------------|----------|
| 4️⃣  | Rotate an Array | Easy | [Java](./Day-4/Solution.java) |
<!-- Add more as you solve -->

---

## 🤝 Contributions

🚀 Want to contribute? Feel free to fork, improve, or add new problems!  
💬 Open an **issue** if you have any suggestions or doubts.

---
📢 Stay tuned for daily updates! 🔥  




class Solution {
    static void rotateArr(int arr[], int d) {
        int n = arr.length;
        d %= n;
        reverse(arr, 0, d - 1);
        reverse(arr, d, n - 1);
        reverse(arr, 0, n - 1);
    }

    static void reverse(int[] arr, int start, int end) {
        while (start < end) {
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            start++;
            end--;
        }
    }
}



# 🔄 Day 4: Rotate an Array

### 📝 Problem Statement
Given an array of size `N` and an integer `D`, rotate the array to the left by `D` positions.

---

### ✅ Solution Approach

1. **Reverse first D elements**
2. **Reverse remaining elements**
3. **Reverse the whole array**

### 📊 Complexity Analysis

- **Time Complexity**: O(N)
- **Space Complexity**: O(1) (In-place)

---



