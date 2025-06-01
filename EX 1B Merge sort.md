# EX 1B Merge Sort

## DATE:04/03/2025

## AIM:

To write a python program to sort the first half of the list using merge sort.

## Algorithm
1.Take a list of numbers as input.

2.If the list has more than one element, divide it into two parts.

3.Recursively sort each part.

4.After both parts are sorted, merge them:

5.Create two temporary lists for the left and right parts.

6.Copy elements from the original list into these temporary lists.

7.Compare elements from both lists and put the smaller one back into the original list.

8.If any elements remain in either list, add them to the original list.

9.Repeat this process until the entire list is sorted.   

## Program:

### Developed by: ABRIN NISHA A
### Register Number: 212222230005
```
def merge(arr,l,m,r):
    n1=m-l+1
    n2=r-m
    L=[0]*(n1)
    R=[0]*(n2)
    for i in range(0,n1):
        L[i]=arr[l+i]
    for j in range(0,n2):
        R[j]=arr[m+1+j]
    i=0
    j=0
    k=l
    while i<n1 and j<n2:
        if L[i]<=R[j]:
             arr[k]=L[i]
             i+=1
        else:
            arr[k]=R[j]
            j+=1
        k+=1
    while i<n1:
        arr[k]=L[i]
        i+=1
        k+=1
    while j<n2:
        arr[k]=R[j]
        j+=1
        k+=1
def mergesort(arr,l,r):
    if l<r:
        m=l+(r-l)//2
     
        mergesort(arr,m+1,r)
        merge(arr, l, m, r)
arr = []
n =int(input())
for i in range(n):
    arr.append(int(input()))
print("Given array is")
for i in range(n):
    print("%d" % arr[i],end=" ")
print("")
mergesort(arr, 0, n-1)
print("\nSorted array is")
for i in range(n):
    print("%d" % arr[i],end=" ")
```

## Output:

![image](https://github.com/user-attachments/assets/6b318155-c929-40d9-b339-195c4f46e5fa)


## Result:

The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
