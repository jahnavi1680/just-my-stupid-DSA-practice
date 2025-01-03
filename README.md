# just-my-stupid-DSA-practice
this is just me trying to do dsa for the first time (not really but yea)

print("Try selection sort")
arr = [7,467,2,0,4,6]
def sort(array):
    min_ind = 0
    for i in range(len(array)-1):
        for j in range(i+1,len(array)):
            if array[j]<array[min_ind]:
                min_ind = j
        min_val = array[min_ind]
        array[min_ind]=array[i]
        array[i]=min_val
    return array
print(sort(arr))


print("Try simple bubble sort")
print('we go from the starting, scan, swaps, repeat')
arr = [7,467,2,0,4,6]

def sort(array):
    for i in range(len(array)-2):
        for j in range(len(array)-1):
            if array[j]>array[j+1]:
                array[j],array[j+1]=array[j+1],array[j]
    return array
print(sort(arr))


print("Try prabably less time taking bubble sort")
print('simple -- we go from the starting, scan, swaps, repeat')
print('we cut down scanning the parts that need not be scanned anymore.. first step is to reduce inner loop by 1 every time')
arr = [7,467,2,0,4,6]
def sort(array):
    for i in range(len(array)-2):
        for j in range(len(array)-1-i):
            if array[j]>array[j+1]:
                array[j],array[j+1]=array[j+1],array[j]
    return array
print(sort(arr))
