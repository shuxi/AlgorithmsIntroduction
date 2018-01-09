#coding=utf-8
from random import randint

def quicksort(array,p,r):
    if p<r:
        q = partition(array,p,r)
        quicksort(array,p,q-1)
        quicksort(array,q+1,r)

def tail_recursive_quicksort(array,p,r):
    while p<r:
        q = partition(array,p,r)
        tail_recursive_quicksort(array,p,q-1)
        p = q+1

#划分数组，返回临界点p，满足:array[i...p] <= array[p+1...r]
def partition(array,p,r):
    x = array[r]
    j = p-1
    for i in range(p,r):
        if array[i] < x:
            j += 1
            array[j],array[i] = array[i],array[j]
    array[j+1],array[r] = array[r],array[j+1]
    return j+1

#产生随机索引，作为划分数组的主元
def random_partirion(array,p,r):
    i = randint(p,r)
    array[i],array[r] = array[r],array[i]
    partition(array,p,r)

if __name__ == "__main__":
    a = [4, 1, 3, 2, 16, 9, 10, 14, 8, 7]
    quicksort(a,0,len(a)-1)
    print(a)
