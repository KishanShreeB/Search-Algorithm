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
Developed by:Kishan Shree B
RegisterNumber: 23012867
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
    
array = eval(input())
k=int(input())
n=len(array)
array.sort()

result = linearSearch(array,n,k)

if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:Kishan Shree B
RegisterNumber: 23012867
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high - low)//2
        if array [mid]==k:
            return mid
        elif array[mid]<k:
            low = mid +1
        else:
            high = mid -1
    return -1
array=eval(input())
array.sort()
k=int(input())

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
Developed by: your name:Kishan Shree B
RegisterNumber: 23012867
'''
def binarySearch(arr, k, low, high):
    if high >=low:
        mid=low+(high-low)//2
        if array [mid]== k:
            return mid
        elif array [mid]>k:
            return binarySearch(array,k,low,mid-1)
        else:
            return binarySearch(array,k,mid+1,high)
    return -1
array=eval(input())
array.sort()
k=int(input())

result=binarySearch(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
## Sample Input and Output
![Screenshot 2023-12-24 133716](https://github.com/KishanShreeB/Search-Algorithm/assets/144870434/c2597573-13f7-4b0b-a017-28aee0bb7fca)

![Screenshot 2023-12-24 133305](https://github.com/KishanShreeB/Search-Algorithm/assets/144870434/236fe4f9-2462-47f7-8113-f53df5c45b32)

![Screenshot 2023-12-24 133329](https://github.com/KishanShreeB/Search-Algorithm/assets/144870434/5192f373-9f0b-4c66-8ce1-2ecb3b6ffedb)

![Screenshot 2023-12-24 133353](https://github.com/KishanShreeB/Search-Algorithm/assets/144870434/5f44194a-9185-4aaa-a204-d31e4939e665)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.
