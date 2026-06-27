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
def linear_search(lst, item):
    lst.sort()   

    print(lst)

    for i in range(len(lst)):
        if lst[i] == item:
            print("Element found at index: ", i)
            return

    print("Element not found")


lst = eval(input())
item = int(input())

linear_search(lst, item)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binary_search(lst, item):
    lst.sort()
    print(lst)
    
    low = 0
    high = len(lst) - 1
    
    while low <= high:
        mid = (low + high) // 2
        
        if lst[mid] == item:
            print("Element found at index: ", mid)
            return
        elif lst[mid] < item:
            low = mid + 1
        else:
            high = mid - 1
    
    print("Element not found")

lst = eval(input())
item = int(input())

binary_search(lst, item)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def binary_search_recursive(lst, item, low, high):
    if low > high:
        return -1

    mid = (low + high) // 2

    if lst[mid] == item:
        return mid
    elif lst[mid] < item:
        return binary_search_recursive(lst, item, mid + 1, high)
    else:
        return binary_search_recursive(lst, item, low, mid - 1)

lst = eval(input())
item = int(input())

lst.sort()
print(lst)

index = binary_search_recursive(lst, item, 0, len(lst) - 1)

if index != -1:
    print("Element found at index: ", index)
else:
    print("Element not found")
```
## Sample Input and Output
i)	#Use a linear search method to match the item in a list.
<img width="1326" height="811" alt="Screenshot 2026-06-27 134157" src="https://github.com/user-attachments/assets/9657a264-c0e3-4259-b223-b0c11bc6edcf" />

ii)	# Find the element in a list using Binary Search(Iterative Method).
<img width="1352" height="820" alt="Screenshot 2026-06-27 134401" src="https://github.com/user-attachments/assets/4e0fd729-d3e8-42a3-9115-03482c4780d5" />

iii)	# Find the element in a list using Binary Search (recursive Method).
<img width="1342" height="822" alt="Screenshot 2026-06-27 134615" src="https://github.com/user-attachments/assets/d5988f70-d964-49f4-aa56-63fad1817408" />

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
