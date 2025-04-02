# GFG 160-Days Problem Solving Challenge

## 📅 Day 6: Majority Element II

### 🚀 Problem Statement
Given an integer array `nums[]` of size `n`, find all elements that appear **more than `n/3` times** in the array.

**Note:** The output should be sorted in increasing order.

### 🔹 Example
#### Input:
```plaintext
nums = [3,2,3]
```
#### Output:
```plaintext
[3]
```

#### Input:
```plaintext
nums = [1,1,1,3,3,2,2,2]
```
#### Output:
```plaintext
[1,2]
```

---

## 🛠 Approach
- **Boyer-Moore Voting Algorithm** is used to find up to two majority elements.
- First pass determines the potential majority candidates.
- Second pass verifies if the candidates actually appear more than `n/3` times.
- Store the results in a sorted list.

### 📝 Code Implementation
#### Java Solution ☕
```java
import java.util.*;

class Solution {
    // Function to find the majority elements in the array
    public List<Integer> findMajority(int[] nums) {
        int num1=Integer.MIN_VALUE,num2=Integer.MIN_VALUE;
        int c1=0 , c2=0;
        int n=nums.length;
        
        for(int x : nums){
            if(x == num1){
                c1++;
            }
            else if(x == num2){
                c2++;
            }
            else if(c1==0){
                num1=x;
                c1=1;
            }
            else if(c2==0){
                num2=x;
                c2=1;
            }
            else{
                c1--;
                c2--;
            }
        }
        
        c1 = c2 = 0;
        for(int x : nums){
            if(x == num1) {
                c1++;
            }
            else if(x == num2) {
                c2++;
            }
        }
        
        List<Integer> res = new ArrayList<>();
        if(c1 > n/3) res.add(num1);
        if(c2 > n/3) res.add(num2);
        
        Collections.sort(res);
        return res;
    }
}
```

---

## ⏳ Complexity Analysis
- **Time Complexity**: O(n) → Two passes through the array.
- **Space Complexity**: O(1) → Constant extra space used.

---

## 🔗 Related Links
- [GeeksforGeeks Problem Link](https://www.geeksforgeeks.org/) *(Replace with the actual problem link)*
- [Boyer-Moore Voting Algorithm](https://en.wikipedia.org/wiki/Boyer%E2%80%93Moore_majority_vote_algorithm)

---

## ⭐ Like this repository?
Give it a ⭐ if you found this helpful!
