# EX 1C Quick Sort
## DATE:
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of string values.

## Algorithm
1. Base Case: If the list has 1 or 0 elements, it is already sorted. Return the list as it is.
2. Partitioning: Select the last element of the list as the pivot.
                 Rearrange the list so that all strings less than or equal to the pivot are on the left side, and all strings greater than the pivot are on the 
                 right side. The pivot is then placed in its correct position.
3. Recursively Sort: Recursively apply the Quick Sort algorithm to the left and right sublists (the parts before and after the pivot).
4.Combine Results: Since the list is sorted in-place, there is no need for merging. The result will be the list sorted in ascending order.
5. Return Sorted List: Return the fully sorted list after recursive partitioning and sorting.
## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of string values.
Developed by: ARUN KUMAR SUKDEV CHAVNA
Register Number: 212222230013
*/
```
```
def quickSort(arr,start,end):
    if end-start>1:
        p=partition(arr,start,end)
        quickSort(arr,start,p)
        quickSort(arr,p+1,end)
def partition(arr,start,end):
    pivot=arr[start]
    i=start+1
    j=end-1
    while True:
        while i<=j and arr[i]<=pivot:
            i=i+1
        while i<=j and arr[j]>=pivot:
            j=j-1
        if i<j:
            arr[i],arr[j]= arr[j],arr[i]
        else:
            arr[start],arr[j]=arr[j],arr[start]
            return j
n=int(input())
arr=[]
for i in range(0,n):
    arr.append(input())
quickSort(arr,0,n)
print("Sorted array is:")
for i in arr:
    print(i)
```
## Output:
![image](https://github.com/user-attachments/assets/48d6c9e2-34b6-45c6-a4d1-61df4fc86fa4)

## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
