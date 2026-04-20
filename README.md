Longest Common Substring & Longest Increasing Subsequence (DAA Project)
Analysis of Longest Common Substring (LCS) and Longest Increasing Subsequence (LIS) using Brute Force, Memoization, and Dynamic Programming

Project Description
This project focuses on solving two important Dynamic Programming problems from Design and Analysis of Algorithms:

 Longest Common Substring (LCS)
 Longest Increasing Subsequence (LIS)
Both problems are implemented using multiple approaches:

Brute Force
Memoization (Top-Down DP)
Tabulation (Bottom-Up DP)

The project also compares their time complexity and performance using experimental datasets.

Objectives:
Main objectives of this project:

Implement LCS and LIS algorithms
Compare brute force and DP approaches
Reduce computational complexity using DP
Analyze runtime performance
Demonstrate overlapping subproblems concept
Study optimal substructure property
Problem 1: Longest Common Substring (LCS)

Problem Statement:

Given two strings, the task is to find the longest continuous substring common to both strings.
Example:

String 1: battery
String 2: cattersion
Output: atter
Characters must:
Appear in the same order
Be continuous
Exist in both strings
Dynamic Programming is used to avoid repeated calculations.

Approaches Used for LCS:

Brute Force Approach
Steps:
Generate all substrings
Compare with second string
Track longest match
Time Complexity:
O(n² × m)
Space Complexity:
O(n²)

Dynamic Programming Approach
DP Rule:
If characters match:
dp[i][j] = dp[i-1][j-1] + 1
Else:
dp[i][j] = 0
Time Complexity:
O(m × n)
Space Complexity:
O(m × n)

Memoization Approach:
Formula:
L(i, j) = 1 + L(i-1, j-1)  (if characters match)
L(i, j) = 0                (otherwise)
Time Complexity:
O(m × n)
Space Complexity:
O(m × n)
Problem 2: Longest Increasing Subsequence (LIS)

Problem Statement:

Given an array of numbers, find the longest increasing subsequence where:
Elements remain in original order
Elements are strictly increasing
Continuity is NOT required
Example:
Input: [5,2,8,6,3,9,7]
Output: [2,3,6,9]
Length = 4
Multiple LIS may exist, but only maximum length is considered.

Approaches Used for LIS:

Brute Force Approach
Steps:
Generate all subsequences
Check increasing order
Select longest valid subsequence
Time Complexity:
O(n × 2ⁿ)
Space Complexity:
O(n)

Dynamic Programming (Tabulation):
DP Rule:
dp[i] = length of LIS ending at index i
Transition:
If arr[j] < arr[i]:
dp[i] = max(dp[i], dp[j] + 1)
Time Complexity:
O(n²)
Space Complexity:
O(n)

Memoization Approach:
Uses recursion + caching:
dp[i] = max LIS ending at index i
Each state solved once.
Time Complexity:
O(n²)
Space Complexity:
O(n)

Approach	Time Complexity	Space Complexity
LCS Brute Force	O(n² × m)	O(n²)
LCS DP	O(m × n)	O(m × n)
LIS Brute Force	O(n × 2ⁿ)	O(n)
LIS DP	O(n²)	O(n)
Dynamic Programming significantly improves performance compared to brute force methods.

Dataset Used:

Performance testing performed using:
input_10.xlsx
lcs_50_100.xlsx
These datasets help measure execution time differences between approaches.
How to Run the Project
Install dependencies:
pip install pandas openpyxl
Run LIS program:
python lis_dp.py
Run LCS program:
python lcs_dp.py
Make sure dataset file paths are correctly updated.

Results:

Experimental results show:
Brute force becomes inefficient for large inputs
DP reduces computation significantly
Memoization avoids repeated calculations
Tabulation provides fastest stable solution
Performance graphs comparing brute force vs DP are included in the project report (see charts in LIS analysis pages near the end of the report).

Advantages:

Demonstrates multiple algorithmic strategies
Shows DP optimization clearly
Reduces exponential complexity
Suitable for large datasets
Useful for real-world sequence analysis problems

Limitations:

Brute force impractical for large inputs
DP requires extra memory
Memoization depends on recursion stack

Applications:

These algorithms are used in:
Bioinformatics (DNA sequence matching)
Text comparison tools
Version control systems
Data compression
Pattern recognition
Machine learning preprocessing

Conclusion:

This project demonstrates how Dynamic Programming techniques efficiently solve sequence-based optimization problems such as Longest Common Substring and Longest Increasing Subsequence. Compared to brute force methods, DP significantly reduces time complexity and improves scalability for large datasets.
