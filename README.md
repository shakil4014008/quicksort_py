# quicksort_py

````py
class QuickSort:
  def __init__(self, arr):
    self.arr = arr

  def sort(self, lo, hi):
    if lo < hi:
      idx = self.partition(lo, hi)
      self.sort(lo, idx-1)
      self.sort(idx+1, hi)
    
  def partition(self, lo, hi):
    pivot = self.arr[hi]
    i,j = lo,lo
    while j < hi:
      if self.arr[j] < pivot:
        self.arr[i],self.arr[j] = self.arr[j],self.arr[i]
        i += 1
      j += 1
    self.arr[i], self.arr[hi] = self.arr[hi], self.arr[i]
    return i

arr = [30,15,17,29,35,20]
obj = QuickSort(arr)
obj.sort(0,5)
print(arr)
````
