 ## 1. Two Pointers

### Valid Palindrome
Write a function that takes a string, s, as an input and determines whether or not it is a palindrome.

### Valid Palindrome II
Write a function that takes a string as input and checks whether it can be a valid palindrome by removing at most one character from it.

### Sum of 3 values
Given an integer array `nums`, find and return all unique triplets `[nums[i], nums[j], nums[k]]`, where the indexes satisfy `i`≠=`j`, `i`≠=`k`, and `j`≠=`k`, and the sum of the elements `nums[i] + nums[j] + nums[k] == 0`.

### Remove nth Node from End of List 
Given the `head` of a singly linked list, remove the nthnth node from the end of the list and return its head.

### Sort Colors
Given an array, `colors`, which contains a combination of the following three elements: -   00 (representing red) -   11 (representing white) -   22 (representing blue)
Sort the array in place so that the elements of the same color are adjacent, with the colors in the order of red, white, and blue. To improve your problem-solving skills, do not utilize the built-in sort function.

### LCA of a Binary Tree 
You are given two nodes, p and q. The task is to return their lowest common ancestor (LCA). Both nodes have a reference to their parent node. The tree’s root is not provided; you must use the parent pointers to find the nodes’ common ancestor.

### Valid Word Abbreviation
Given a string word and an abbreviation abbr, return TRUE if the abbreviation matches the given string. Otherwise, return FALSE. The following are not valid abbreviations: a) "c06r" (has leading zeroes) b) "cale0ndar" (replaces an empty string) c) "c24r" ("c al enda r" the replaced substrings are adjacent)

## 2. Fast and Slow Pointers
```
FUNCTION fastAndSlow(dataStructure):

  # initialize pointers (or indices)

  fastPointer = dataStructure.start   # or 0 if the data structure is an array

  slowPointer = dataStructure.start   # or 0 if the data structure is an array

  WHILE fastPointer != null AND fastPointer.next != null: 

    # For arrays: WHILE fastPointer < dataStructure.length AND (fastPointer + 1) < dataStructure.length:

    slowPointer = slowPointer.next            

    # For arrays: slowPointer = slowPointer + 1

    fastPointer = fastPointer.next.next       

    # For arrays: fastPointer = fastPointer + 2

    IF fastPointer != null AND someCondition(fastPointer, slowPointer):

      # For arrays: use someCondition(dataStructure[fastPointer], dataStructure[slowPointer]) if needed

      handleCondition(fastPointer, slowPointer)

      BREAK

  # process the result

  processResult(slowPointer)

  # For arrays: processResult(slowPointer) might process dataStructure[slowPointer]

```

### Find the Duplicate 
Given an array of positive numbers, `nums`, such that the values lie in the range [1,n][1,n], inclusive, and that there are n+1n+1 numbers in the array, find and return the duplicate number present in `nums`. There is only one repeated number in `nums`, but it may appear more than once in the array.

## 3. Sliding Window
'''
FUNCTION slidingWindow(arr, k, processWindow):

  # Initialize the window result (sum, product, count, etc.)

  windowResult = INITIAL_VALUE

  # Compute the initial window's result

  FOR i FROM 0 TO k - 1:

    UPDATE windowResult WITH arr[i]

  # Process the first window

  processWindow(windowResult)

  # Slide the window across the array

  FOR i FROM k TO length of arr - 1:

    UPDATE windowResult BY ADDING arr[i]  # Add a new element to the window

    UPDATE windowResult BY REMOVING arr[i - k]  # Remove outgoing element

    processWindow(windowResult)  # Operation on the updated window
    
'''
### Longest Substring without Repeating Characters
Given a string, input_str, return the length of the longest substring without repeating characters.
### Longest Repeating Character Replacement
Given a string `s` and an integer `k`, find the length of the longest substring in `s`, where all characters are identical, after replacing, at most, `k` characters with any other lowercase English character.
### Minimum Size Subarray Sum
Given an array of positive integers, nums, and a positive integer, target, find the minimum length of a contiguous subarray whose sum is greater than or equal to the target. If no such subarray is found, return 0

## 4. Merge Intervals
## Merge Intervals
We are given an array of closed intervals, `intervals`, where each interval has a start time and an end time. The input array is sorted with respect to the start times of each interval. For example, `intervals` = [[1,4],[3,6],[7,9]][ [1,4], [3,6], [7,9] ] is sorted in terms of start times 1,31, 3, and 77.
Your task is to merge the overlapping intervals and return a new output array consisting of only the non-overlapping intervals.
## Interval List Intersection 
For two lists of closed intervals given as input, `interval_list_a` and `interval_list_b`, where each interval has its own start and end time, write a function that returns the intersection of the two interval lists.
For example, the intersection of [3,8][3,8] and [5,10][5,10] is [5,8][5,8].
## Insert Interval 
Given a sorted list of nonoverlapping intervals and a new interval, your task is to insert the new interval into the correct position while ensuring that the resulting list of intervals remains sorted and nonoverlapping. Each interval is a pair of nonnegative numbers, the first being the start time and the second being the end time of the interval.
## Meeting Rooms II
We are given an input array of meeting time intervals, intervals, where each interval has a start time and an end time. Your task is to find the minimum number of meeting rooms required to hold these meetings.

