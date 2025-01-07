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

print("Try insertion sort")
arr = [7,467,2,0,4,6]
def sort(array):
    for i in range(len(arr)-1):
        hole = i+1
        el = array[hole]
        #shift
        while hole>0 and array[hole-1]>el:
            array[hole]=array[hole-1]
            hole -= 1
        array[hole]=el
    return array
print(sort(arr))


print("Try merge sort")
arr = [7,467,2,0,4,6]
a = [2,5,7,8]
b = [3,6,9,10]
def merge(a,b):
    i=0
    j=0
    k=0
    full = [0] * (len(a) + len(b))
    while i<len(a) and j<len(b):
        if a[i]>b[j]:
            full[k] = b[j]
            j += 1
        else: 
            full[k]=a[i]
            i += 1
        k+=1
    if i<len(a):
        full[k:] = a[i:]
    elif j<len(b):
        full[k:] = b[j:]
    return full
def mergesort(array):
    div = len(array)//2
    left = array[:div]
    right = array[div:]
    if (len(left)>1):
        left = mergesort(left)
    if (len(right)>1):
        right = mergesort(right)
    print(merge(left,right))
    return merge(left,right)
print(mergesort(arr))



