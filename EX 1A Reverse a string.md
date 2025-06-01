# EX 1A Reverse a String

## DATE: 04/03/2025

### AIM:

To write a program to create a recursive function to reverse a string.

### Algorithm :
1.Start the program.

2.Define a function that takes a string as input.

3.If the string is empty or has only one character, return it as it is.

4.Otherwise, take the last character of the string.

5.Call the same function with the rest of the string (excluding the last character).

6.Add the last character to the result of the recursive call.

7.Return the final reversed string.

8.Get input from the user.

9.Call the function with the user's input.

10.Print the reversed string.

11.End the program.

### Program:
Program to implement Reverse a String

### Developed by: ABRIN NISHA A
### Register Number: 212222230005
```

def rev(s):
    if(len(s)<1):
        return s
    return s[-1]+rev(s[:-1])
s=input()
print(rev(s))

```
### Output:

![Screenshot 2025-04-29 142942](https://github.com/user-attachments/assets/c191ad44-8f10-4593-aa31-cd2996a9ed3d)


### Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
