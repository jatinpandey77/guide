---
title: Bubble Sort
---
## Bubble Sort

Bubble Sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in wrong order.

This is a very slow sorting algorithm compared to algorithms like quicksort, with worst-case complexity O(n^2). However, the tradeoff is that bubble sort is one of the easiest sorting algorithms to implement from scratch.

### Example:

#### First Pass:
( 5 1 4 2 8 ) –> ( 1 5 4 2 8 ), Here, algorithm compares the first two elements, and swaps since 5 > 1.

( 1 5 4 2 8 ) –> ( 1 4 5 2 8 ), Swap since 5 > 4

( 1 4 5 2 8 ) –> ( 1 4 2 5 8 ), Swap since 5 > 2

( 1 4 2 5 8 ) –> ( 1 4 2 5 8 ), Now, since these elements are already in order (8 > 5), algorithm does not swap them.


#### Second Pass:

( 1 4 2 5 8 ) –> ( 1 4 2 5 8 )

( 1 4 2 5 8 ) –> ( 1 2 4 5 8 ), Swap since 4 > 2

( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )

( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )

Now, the array is already sorted, but our algorithm does not know if it is completed. The algorithm needs one whole pass without any swap to know it is sorted.

#### Third Pass:

( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )

( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )

( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )

( 1 2 4 5 8 ) –> ( 1 2 4 5 8 )

#### Properties
- Space complexity: O(1)
- Best case performance: O(n)
- Average case performance: O(n\*n)
- Worst case performance: O(n\*n)
- Stable: Yes

### Video Explanation
[Bubble sort in easy way](https://www.youtube.com/watch?v=Jdtq5uKz-w4)

This code will use bubble sort to sort the array.
```js
let arr = [1, 4, 7, 45, 7,43, 44, 25, 6, 4, 6, 9];
let sorted = false

while(!sorted) {
  sorted = true
  for(var i=0; i < arr.length; i++) {
    if(arr[i] < arr[i-1]) {
      let temp = arr[i];
      arr[i] = arr[i-1];
      arr[i-1] = temp;
      sorted = false;
    }
  }
}
```

Here is the algorithm written in Java.

```java
public class bubble-sort {
    static void sort(int[] arr) {
        int n = arr.length;
        int temp = 0;
         for(int i=0; i < n; i++){
                 for(int x=1; x < (n-i); x++){
                          if(arr[x-1] > arr[x]){
                                 temp = arr[x-1];
                                 arr[x-1] = arr[x];
                                 arr[x] = temp;
                         }

                 }
         }

    }
    public static void main(String[] args) {

		for(int i=0; i < 15; i++){
			int arr[i] = (int)(Math.random() * 100 + 1);
		}

                System.out.println("array before sorting\n");
                for(int i=0; i < arr.length; i++){
                        System.out.print(arr[i] + " ");
                }
                bubbleSort(arr);
                System.out.println("\n array after sorting\n");
                for(int i=0; i < arr.length; i++){
                        System.out.print(arr[i] + " ");
                }

        }
}
```

### Optimized Implementation:
The above function always runs O(n^2) time even if the array is sorted. It can be optimized by stopping the algorithm if inner loop didn’t cause any swap.

Optimized Algorithm written in C

```C
void bubbleSort(int a[], int n) { 
   int i, j; 
   bool swapped; 
   for (i = 0; i < n - 1; i++) { 
     swapped = false; 
     for (j = 0; j < n-i-1; j++) { 
        if (a[j] > a[j+1]) { 
           swap(&a[j], &a[j+1]); 
           swapped = true; 
        } 
     } 
     if (swapped == false) // if no swaps, stop algorithm
        break; 
   } 
} 
```
#### Worst and Average Case Time Complexity: O(n*n).
#### Best Case Time Complexity: O(n). Best case occurs when array is already sorted.

### More Information
<!-- Please add any articles you think might be helpful to read before writing the article -->
- [Wikipedia](https://en.wikipedia.org/wiki/Bubble_sort)
- [Bubble Sort Algorithm - CS50](https://youtu.be/Ui97-_n5xjo)
- [Bubble Sort Algorithm - GeeksForGeeks (article)](http://www.geeksforgeeks.org/bubble-sort)
- [Bubble Sort Algorithm - MyCodeSchool (video)](https://www.youtube.com/watch?v=Jdtq5uKz-w4)
- [Algorithms: Bubble Sort - HackerRank (video)](https://www.youtube.com/watch?v=6Gv8vg0kcHc)
- [Bubble Sort Algorithm - GeeksForGeeks (video)](https://www.youtube.com/watch?v=nmhjrI-aW5o)
