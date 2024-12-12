Heap-Sort Algorithm

(a) Algorithms:
The Heap-Sort algorithm involves two main steps:
1.	Building the Max-Heap:
-	Rearrange the elements of the array to satisfy the Max-Heap property.
-	Use the heapify function to ensure each subtree is a valid Max-Heap.
2.	Sorting:
-	Repeatedly extract the largest element (root of the heap) by swapping it with the last element in the heap.
- Reduce the size of the heap and reapply heapify to maintain the Max-Heap property.   

Pseudo Code
  1. Build a Max-Heap from the input array.
     For i = (n / 2 - 1) down to 0:
         Heapify(array, n, i)
  2. Repeat the following steps until the heap size is 1:
     For i = n - 1 down to 1:
         Swap(array[0], array[i]) // Swap the root with the last element
         Heapify(array, i, 0) // Restore Max-Heap property for the reduced heap


(b) Analysis of Heap-Sort:
1.	Time Complexity:
-	Building the Heap: O(n)
-	Heapify during sorting: For n elements, each  heapify operation takes O(log n). Thus, sorting O(n log n).
-	Total Time Complexity: O(n log n)
2.	Space Complexity:
-	Heap-Sort is an in-place algorithm, so it requires only O(1) extra space.
3.	Stability:
       Heap-Sort is not stable since element positions are swapped in a Max-Heap structure.
