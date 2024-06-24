Minimize the Maximum Difference between Heights
In this we need to either increase or decrease the height of every tower by k (only once) where k > 0. The task is Python Program to Minimize the Maximum Difference between Heights of the longest and the shortest tower after modifications print out this difference.

Input : arr = [2, 16, 9], k = 6
Output : Maximum difference is 5.
Explanation : We change 2 to 8, 16 to 10 and 9 to 15. Maximum difference is 7
(between 8 and 15). We can’t get a lower difference.
Minimize the maximum difference between the heights in python
Algorithm
Start by passing array and value of k to function
Declare a variable n and assign half the sum of minimum and maximum element of array
Declare a empty list name new to store modified array
Iterate for all the element in array
If difference between maximum and minimum element of array is less then k then return the difference between max and min of array
Else if, the current element is greater then or equals to n then append the defense between current element and k to new array
Else append the sum of current element and k to new array
Return the difference between maximum and minimum element of new array
Print the returned value by the function
Space & Time Complexity
Time Complexity: O(nlogn)
Space Complexity: O(n)
Python Program to Minimize the maximum difference between the height
Python Code
Run
def profit(arr, k):
    n = (min(arr) + max(arr)) // 2
    new = []
    for i in arr:
        if max(arr) - min(arr) < k:
            return max(arr) - min(arr)
        elif i >= n:
            new.append(i - k)
        else:
            new.append(i + k)
    return max(new) - min(new)


array = [2, 9, 16]
K = 6
print("Maximum difference is :", profit(array, K))
Output
Maximum difference is : 7
