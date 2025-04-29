# EX 1A Reverse a String
## DATE:
## AIM:
To use recursion to write a Python function for determining if a string has more vowels than consonants return True otherwise False.

## Algorithm
1. Base Case: If the string has only one character, check if it is a vowel ('a', 'e', 'i', 'o', 'u'). Return 1 for a vowel and 0 for a consonant.

2. Recursive Split: If the string has more than one character, divide the string into two halves.

3. Count Vowels Recursively: Recursively count the vowels in both halves of the string.

4. Combine Results: Add the vowel counts from both halves to get the total number of vowels in the string.

5. Comparison: If the total number of vowels is greater than the number of consonants, return True. Otherwise, return False. 

## Program:
```
/*
Program to write a Python function for determining if a string has more vowels than consonants 
Developed by: ARUN KUMAR SUKDEV CHAVAN
Register Number:  212222230013
*/
```
```
def vowels1(str):
    def count(str):
        size=len(str)
        if(size==1):
            if(str.lower() in ['a','e','i','o','u']):
                return 1
            return 0
        vowels_a=count(str[0:size//2])
        vowels_b=count(str[size//2:size])
        return vowels_a+vowels_b
    vowels=count(str)
    if(vowels>len(str)-vowels):
        return True
    return False
str=input()
print(vowels1(str))
```

## Output:
![image](https://github.com/user-attachments/assets/e8d33784-fb9f-44ef-96a9-e8d90aff55e6)

## Result:
The program successfully determines if a string has more vowels than consonants.
