# Assignment-2ImplementBinarySearch
def binary_search(list_arr, x):
    low = 0
    high = len(list_arr)-1
    mid = 0

    while low <= high:

        mid = (high + low) // 2

        if list_arr[mid] < x:
            low = mid + 1

        elif list_arr[mid] > x:
            high = mid - 1

        else:
            return mid

    return -1


arr = [2, 3, 4, 10, 40]
x = 40

result = binary_search(arr, x)

if result != -1:
    print("Element is present at index", str(result))
else:
    print("Element is not present in array")
