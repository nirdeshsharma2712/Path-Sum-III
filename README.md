# 📊 LeetCode Problem: Path Sum III

## 🧩 Problem Statement

Given the `root` of a **binary tree** and an integer `targetSum`, return the **number of paths** where the sum of the values along the path equals `targetSum`.

> **Note :**
> - The path does not need to start or end at the root or a leaf, but it must go downwards (i.e., traveling only from parent nodes to child nodes).



## 🧠 Approach: Recursive Approach

- At each `node`, push its value into a **vector** (this stores the path we’re currently exploring).

- Call the function for **left** and **right** child.

- After both calls , traverse the vector from the end (leaf side) to the start and keep **summing values**.

- If at any point the running **sum equals the targetSum**, increment the **count**.

- Pop the last element from the **vector** to restore the path for other branches.



## ✅ Example Walkthrough

### Example 1

##### Input: root = [10,5,-3,3,2,null,11,3,-2,null,1], targetSum = 8
##### Output: 3

##### Explanation: 
<pre> 
  - The paths that sum to 8 are shown.
</pre>

### Example 2

##### Input: root = [5,4,8,11,null,13,4,7,2,null,null,5,1], targetSum = 22
##### Output: 3


## 🛠️ Constraints

- The number of nodes in the tree is in the range `[0, 1000]`
- `-10^9 <= Node.val <= 10^9`
- `-1000 <= targetSum <= 1000`
