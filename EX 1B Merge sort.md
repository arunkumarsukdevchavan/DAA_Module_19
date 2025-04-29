# EX 1B Merge Sort
## DATE:
## AIM:
To Write a python program for the implementation of merge sort on the given list of float values.

## Algorithm
1. Base Case: If the list has 1 or 0 elements, it is already sorted. Return the list as it is.
2. Divide: Find the middle index of the list. Divide the list into two halves, left and right, around the middle.
3. Recursively Sort: Recursively apply Merge Sort to both the left and right halves of the list.
4. Merge: Merge the two sorted halves back together. Compare the elements from the left and right halves, and add the smaller element to the result list.
5. Return Sorted List: Return the merged, sorted list as the final output.  
## Program:
```
/*
Program to implement Merge Sort
Developed by: ARUN KUMAR SUKDEV CHAVAN
Register Number: 212222230013
*/
```
```
def mergesort(arr):
    size=len(arr)
    if(size>1):
        mid=size//2
        leftarr=arr[:mid]
        rightarr=arr[mid:]
        mergesort(leftarr)
        mergesort(rightarr)
        i=0
        j=0
        k=0
        while(i<len(leftarr) and j<len(rightarr)):
            if(leftarr[i]<rightarr[j]):
                arr[k]=leftarr[i]
                i+=1
                k+=1
            else:
                arr[k]=rightarr[j]
                j+=1
                k+=1
        while(i<len(leftarr)):
            arr[k]=leftarr[i]
            i+=1
            k+=1
        while(j<len(rightarr)):
            arr[k]=rightarr[j]
            j+=1
            k+=1
n=int(input())
arr=[]
for i in range(n):
    num=float(input())
    arr.append(num)
print("Given array is ")
for i in range(n):
    print(arr[i],end=" ")
mergesort(arr)
print("\nSorted array is ")
for i in range(n):
    print(arr[i],end=" ")
        
```
## Output:

![image](https://github.com/user-attachments/assets/0382b942-2bfb-4b5f-a85e-a3a1b4175466)


## Result:
The program successfully sorts the given list of float values using the Merge Sort algorithm, where the list is recursively divided into halves, each half is sorted, and then the sorted halves are merged back together to form the final sorted list.
