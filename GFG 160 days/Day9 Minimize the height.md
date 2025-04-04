# GeeksforGeeks 160 Days of Problem Solving

This repository contains solutions to the **GeeksforGeeks 160 Days Problem Solving Challenge**, implemented in **Java**. Each solution is optimized and well-documented for better understanding.

---

## 🔹 Day 9: Minimize the Heights

### 🧠 Problem Statement
Given an array `arr[]` of size `n` and an integer `k`, modify each element of the array either by **adding** or **subtracting** `k`. The goal is to **minimize the difference** between the maximum and minimum elements after modification.

### 📥 Example
```java
Input: arr = [1, 5, 8, 10], k = 2
Output: 5
Explanation: Modified array [3, 3, 6, 8] gives min difference = 8 - 3 = 5.
```

---

## ✅ Java Solution
```java
class Solution {
    int getMinDiff(int[] arr, int k) {
       int n = arr.length;
       List<int[]> modifiedHeights = new ArrayList<>();
       int[] frequency = new int[n];
       
       for (int i = 0; i < n; i++) {
           if (arr[i] - k >= 0) {
               modifiedHeights.add(new int[]{arr[i] - k, i});
           }
           modifiedHeights.add(new int[]{arr[i] + k, i});
       }
       
       modifiedHeights.sort(Comparator.comparingInt(a -> a[0]));
       int left = 0, right = 0, covered = 0, minDifference = Integer.MAX_VALUE;
       
       while (right < modifiedHeights.size()) {
           if (frequency[modifiedHeights.get(right)[1]]++ == 0) {
               covered++;
           }
           while (covered == n) {
               minDifference = Math.min(minDifference, modifiedHeights.get(right)[0] - modifiedHeights.get(left)[0]);
               if (--frequency[modifiedHeights.get(left)[1]] == 0) {
                  covered--;
               }
               left++;
           }
           right++;
       }
       return minDifference;
    }
}
```

---

## 🔍 Approach:
1. **Generate Possible Heights**: Create a list containing possible heights after adding or subtracting `k`.
2. **Sorting**: Sort this list based on height values.
3. **Sliding Window Technique**: Use two pointers (`left` and `right`) to find the smallest possible difference while ensuring all original indices are covered at least once.
4. **Minimization**: Track the minimum difference obtained by shrinking the window when all elements are included.

---

## 📝 Complexity Analysis:
- **Time Complexity**: `O(n log n)` (Sorting the list takes the most time)
- **Space Complexity**: `O(n)` (Storing modified heights)

## 📚 Topics Covered:
- Sorting
- Two-Pointer Technique
- Sliding Window
- Greedy Algorithm

---

## 🚀 More GFG Solutions
Check out the full collection of **GeeksforGeeks 160 Days Challenge** solutions in this repository!

📌 **If you found this helpful, give the repo a ⭐!** 😊

