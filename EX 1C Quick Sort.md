# EX 1C Quick Sort

## DATE: 04/03/2025

## AIM:

To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm :
1.Input the number of elements n, then read n floating-point numbers into a list called arr.

2.Start QuickSort by calling quickSort(arr, 0, n-1) to sort the array from the first to the last index.

3.QuickSort Function:
Base Case Check:
If the list has only one element, it's already sorted—return as is.

4.Recursive Case:
If low < high, continue:

Choose a pivot element and partition the array around it.

Recursively sort the left subarray (elements less than or equal to pivot).

Recursively sort the right subarray (elements greater than pivot).

5.Partition Function:
Select the last element in the subarray as the pivot.

6.Initialize an index i to one position before the start of the subarray.

7.Scan the array from the low index to high - 1

8.After the loop, place the pivot in its correct sorted position by swapping it with the element at index i+1.

9.Return the position (i+1) as the partitioning index.


10.After sorting, print the message: "Sorted array is:"

11.Print each element of the now sorted array.

## Program :

### Developed by: ABRIN NISHA A
### Register Number: 212222230005
```

def partition(arr, low, high):
    i = (low-1)
    pivot = arr[high]

    for j in range(low, high):
        if arr[j] <= pivot:
            i = i+1
            arr[i], arr[j] = arr[j], arr[i]

    arr[i+1], arr[high] = arr[high], arr[i+1]
    return (i+1)

def quickSort(arr, low, high):
    if len(arr) == 1:
        return arr
    if low < high:
        pi = partition(arr, low, high)
        quickSort(arr, low, pi-1)
        quickSort(arr, pi+1, high)

arr = []
n = int(input())
for i in range (n):
    arr.append(float(input()))
#print("Original array is:")
#for i in arr:
#    print(i)
quickSort(arr, 0, n-1)
print("Sorted array is:")
for i in arr:
    print(i)



```

## Output :

![Screenshot 2025-04-29 183323](https://github.com/user-attachments/assets/aae6dbfc-3cec-4e57-8cc5-3f7e8cdbaec7)



## Result :

The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
