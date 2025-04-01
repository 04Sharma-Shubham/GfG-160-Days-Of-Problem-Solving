
# 🚀 GFG 160 Days of DSA Challenge

Welcome to my **GeeksforGeeks 160 Days Problem Solving** repository!  
This repository contains **Java solutions** for each day's problem, along with explanations and complexity analysis.

---

## 📌 Features

- ✅ **160 Days of GFG Problems**
- 🧪 **Optimized Java solutions**
- 📂 **Structured by Day**
- 📊 **Time & Space Complexity Analysis**
- 📝 **Beginner-friendly & Interview-focused**

---

## 📅 Progress Tracker

| Day  | Problem            | Difficulty | Solution |
|------|--------------------|------------|----------|
| 4️⃣  | Rotate an Array    | Easy       | [Java](./Day-4/Solution.java) |
| 5️⃣  | Next Permutation   | Medium     | [Java](./Day-5/Solution.java) |
<!-- Add more as you solve -->

---

## 🤝 Contributions

🚀 Want to contribute? Feel free to **fork**, **improve**, or **add new problems**!  
💬 Open an **issue** if you have any suggestions or doubts.

---
📢 Stay tuned for daily updates! 🔥  
📄 Day-5/Solution.java
java
Copy
Edit
# Solution 
    void nextPermutation(int[] arr) {
        int n = arr.length;
        int i = n - 2, j = n - 1;
        
        while (i >= 0 && arr[i] >= arr[i + 1]) 
            i--;
        
        if (i >= 0) {
            while (arr[j] <= arr[i]) 
                j--;
            
            int temp = arr[i];
            arr[i] = arr[j];
            arr[j] = temp;
        }
        reverse(arr, i + 1, n - 1);
    }

    void reverse(int[] arr, int start, int end) {
        while (start < end) {
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            start++;
            end--;
        }
    }

📄 Day-5/README.md
markdown
Copy
Edit
# 🔄 Day 5: Next Permutation

### 📝 Problem Statement
Given an array `arr` of size `N`, find the **next lexicographical permutation** of the array.

---

### ✅ Solution Approach

1. **Find the rightmost decreasing element** (from the end).
2. **Swap it with the smallest element greater than it** (to maintain order).
3. **Reverse the remaining elements** to get the next permutation.

### 📊 Complexity Analysis

- **Time Complexity**: O(N)
- **Space Complexity**: O(1) (In-place)

---

### 📌 Example
#### **Input**
arr = [1, 2, 3]

markdown
Copy
Edit
#### **Output**
[1, 3, 2]

yaml
Copy
Edit

---

### 🔗 GFG Link
[Next Permutation](https://practice.geeksforgeeks.org/problems/next-permutation)

---

🚀 Keep solving, keep growing! 💪🔥
🎯 Next Steps:
✅ Add badges (Java, Stars, Forks)
✅ Include a progress bar in README
✅ Daily commit updates

Let me know if you need any modifications or help pushing this to GitHub! 🚀
