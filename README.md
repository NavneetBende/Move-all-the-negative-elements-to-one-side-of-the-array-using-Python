Move all the negative elements to one side of the array
User will give an array as input to user. We are required to move all the negative elements to one side of the array, that is either to left or right. We will see various method to do so in this article. 

Example:

array= [1, 3, -1, 4, -3, -5, -6, 3, 7]
After moving all the elements to left array =[-6, -5, -3, -1, 1, 3, 3, 4, 7]
Method 1: Move to left
We will sort the array in ascending order, so that all the negative elements will move to the left side of array as negative element are small.

Algorithm
Step 1: Create and Call a function
Step 2: sort the array and print
move all the elements to one side of array using python
Python Code
Run
def find(arr):
    # sort array
    arr.sort()

    # print array
    print("Array after moving all the elements to left:", arr)


array = [1, 3, -1, 4, -3, -5, -6, 3, 7]
# call function
find(array)
Output
Array after moving all the elements to left: [-6, -5, -3, -1, 1, 3, 3, 4, 7]
Related Pages
Find the “Kth” max and min element of an array 

Move all the negative elements to one side of the array

Find the Union and Intersection of the two sorted arrays

Find Largest sum contiguous Subarray

Minimize the maximum difference between heights 


Method 2: Move to right
We will sort the array in descending order, so that all the negative elements will move to the right side of array.

Algorithm
Step 1: Create and Call a function
Step 2: sort the array in descending order and print
Python Code
Run
def find(arr):
    # sort array
    arr.sort(reverse=True)

    # print array
    print("Array after moving all the elements to right:", arr)


array = [1, 3, -1, 4, -3, -5, -6, 3, 7]
# call function
find(array)
Output
Array after moving all the elements to right: [7, 4, 3, 3, 1, -1, -3, -5, -6]
Method 3: Move to left
Algorithm
Step 1: Declare new array name ans.
Step 2: Iterate on elements of array.
        ->  If the element is less than zero then append that element to ans array.

Step 3: If zero present in array , then append zero in ans array.
Step 4: Iterate on array elements again, if element is greater than zero, then append element to ans array.
Step 5: Print ans array.
Python code
Run
def find(arr):
    ans = []
    for i in arr:
        if i < 0:
            ans.append(i)
        if 0 in arr:
            ans.append(0)
    for i in arr:
        if i > 0:
            ans.append(i)

    print("Array after moving all the elements to right:", ans)


array = [1, 3, -1, 4, -3, -5, -6, 3, 7]
# call function
find(array)
Output
Array after moving all the elements to right: [-1, -3, -5, -6, 1, 3, 4, 3, 7]
Method 4: Move to right
Algorithm
Step 1: Declare new array name ans.
Step 2: Iterate on elements of array.
        -> If the element is less than zero then append that element to ans array.

Step 3: If zero present in array , then append zero in ans array.
Step 4: Iterate on array elements again, if element is greater than zero, then append element to ans array.
Step 5: Reverse the array ans.
Step 6: Print ans array.
Python Code
Run
def find(arr):
    ans = []
    for i in arr:
        if i < 0:
            ans.append(i)
        if 0 in arr:
            ans.append(0)
    for i in arr:
        if i > 0:
            ans.append(i)
    ans = ans[::-1]

    print("Array after moving all the elements to right:", ans)


array = [1, 3, -1, 4, -3, -5, -6, 3, 7]
# call function
find(array)
Output
Array after moving all the elements to right: [7, 3, 4, 3, 1, -6, -5, -3, -1]
