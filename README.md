# Data-Structures
---
## Sorting Algorithms - time complexity

| Algorithm| Best|Average|Worst|
|:---------|:----|:----|:----|
|Selection Sort| O(n^2)|O(n^2)|O(n^2)|
|Bubble Sort| O(n) |O(n^2) | O(n^2)|
|Insertion Sort| O(n) |O(n^2) | O(n^2)|
|Heap Sort| O(nlog(n)) |O(n(log(n)) | O(nlog(n))|
|Quick Sort| O(nlog(n)) |O(n(log(n)) | O(n^2)|
|Merge Sort| O(n(log(n)) |O(n(log(n)) | O(n(log(n))|
|Bucket Sort| O(n+k) |O(n+k) | O(n^2)|
|Radix sort| O(nk)| O(nk) | O(nk)|

### Bubble Sort
---
```python
def bubble_sort(arr):
    n=len(arr)
    for i in range(n):
        swapped=False
        for j in range(n-i-1):
            if arr[j]>arr[j+1]:
                arr[j],arr[j+1]=arr[j+1],arr[j]
                swapped=True
        if swapped==False:
            break

arr=[8,9,1,2,3,10]
bubble_sort(arr)
print(arr)
```
> Best case Time Complexity is O(n) -- occurs when the array already sorted <br />
> Worst Case Time complexity is O(n^2)  -- occures when the array is reverse sorted

### Insertion sort
---
```python
def insertion_sort(arr):
    for i in range(1,len(arr)):
        key=arr[i]
        j=i-1
        while j>=0 and key<arr[j]:
            arr[j+1]=arr[j]
            j-=1
        arr[j+1]=key
    
arr=[5,1,4,2,8]
insertion_sort(arr)
print(arr)
```
