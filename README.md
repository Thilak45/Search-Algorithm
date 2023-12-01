# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by:TILAK VELLACHI
RegisterNumber: 23009564
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
array = eval(input())
k = eval(input())
n=len(array)
array.sort()
result=linearSearch(array,n,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:TILAK VELLACHI
RegisterNumber: 23009564
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array=eval(input())
array.sort()
k=eval(input())
result=binarySearchIter(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
     print(array)
     print("Element found at index: ",result) 
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: your name:TILAK VELLACHI
RegisterNumber: 23009564
'''
def BinarySearch(arr, k, low, high):
    while low<=high:
        mid = low + (high - low)//2
        if arr[mid] == k:
            return mid
        elif arr[mid] < k:
            low = mid + 1
        else:
            high = mid - 1
    return -1
    
arr = eval(input())
arr.sort()
print(arr)
k = eval(input())
result = BinarySearch(arr,k,0,len(arr)-1)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
## Sample Input and Output

![image](https://github.com/Thilak45/Search-Algorithm/assets/138849161/c48ccfe5-81a5-4b70-9d6f-04233f75f209)
![image](https://github.com/Thilak45/Search-Algorithm/assets/138849161/269edc64-94a3-4019-844b-6fe6606a154d)
![image](https://github.com/Thilak45/Search-Algorithm/assets/138849161/05251f6f-d75b-4321-9a13-f688cef8b575)

## OUTPUT:
![image](https://github.com/Thilak45/Search-Algorithm/assets/138849161/498b89ec-cc4e-48ec-8d02-c59381338eaf)
![image](https://github.com/Thilak45/Search-Algorithm/assets/138849161/0e8333ce-933c-4c1a-be89-3e3c3a931588)
![image](https://github.com/Thilak45/Search-Algorithm/assets/138849161/58b1956f-4d11-4d85-8565-f394069c35fd)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
