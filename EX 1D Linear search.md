# EX 1D Linear search
## DATE:
## AIM:
To write a python program for a search function with parameter list name and the value to be searched using float values.
## Algorithm
1. Function Input: The function will take two parameters: the list of float values (list_name) and the value to be searched (search_value).
2. Iterate Through the List: Loop through each element of the list using a loop (e.g., for loop).
3. Compare Each Element: For each element in the list, compare it with the search_value.
4. Return Index if Found: If the element matches the search_value, return the index of that element in the list.
5. Return Not Found: If the loop completes and the value is not found in the list, return a message indicating that the value is not present.  
## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using float values.
Developed by: ARUN KUMAR SUKDEV CHAVAN 
Register Number: 212222230013
*/
```
```
def search(List, n):
    if n in List:
        print(n, "Found")
    else:
        print(n, "Not Found")

List = []
a = int(input())
for i in range(0, a):
    List.append(float(input()))
n=float(input())
```
## Output:
![image](https://github.com/user-attachments/assets/ac6f514e-c237-481f-8a9f-d8a573ed30d5)

## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
