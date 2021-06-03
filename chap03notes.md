# Chapter 3: Algorithms
## Math 275 | Summer 2021
---

## Algorithms
* An algorithm are precise step by step instructions for completing a task.
* Pseudocode is useful for understanding algorithms.
  * Syntax is self-explanatory


### Bubble Sort
* Simple sorting algorithm
* Not that efficient
* Works by iterating through array, and comparing element with the next element, and then switching them if they are not in order.
* In practice, this consists of two nested for loops. The outer for loop iterates through the *length of the array* (you don't actually use its index to swap) to guarantee all elements are swapped, and the inner loop loops from the beginning of the array to the last sorted value and does the actual sorting.
* The inner loop does the actual swapping, you have the outer loop there to make sure the inner loop swaps everything the necessary amount of times. If you didn't have the outer loop, and you looped only once, you'd only guarantee the max element be sorted.
* With each pass of outer for loop, an element is guaranteed to be sorted.
  * Let's say, we are trying to sort the following array: `[2, 3, 4, 1, 5]`.
  * The first outer for loop pass guarantees that the largest element, `5`, is in the correct position.
  * The second outer for loop pass guarantees that the two largest elements, `4`, `5`, are in their correct positions.
  * The third outer for loop guarantees that the three largest elements, `3`, `4`, and `5`, are in their correct positions.
  * >The fourth pass consists of one comparison, namely, the comparison of `1` and `2`. Because `1` < `2`, these elements are in the correct order. This completes the bubble sort.
* This is why the outer loop exists: to guarantee more and more numbers being sorted. Thus you iterate over the length of the array, so you can make sure that length is sorted.
* Because with each pass, we have more and more numbers that are sorted, the inner loop doesn't need to iterate over those sorted values. Thus it just needs to iterate through the beginning to the last unsorted value.
* You can think of each pass of the inner loop, as going over a new smaller array (new and smaller because it's not going over the last element), and pushing that max value to the end. Once it pushes that max value end, it goes over the array again (but without what it just pushed to the end, so it's like it's iterating over a newer smaller array), and then pushes the new max to the end. It then does this again and again until the array's size becomes 0.

Example implementation assuming, `swap()` function is defined and implemented:

~~~C++
void bubbleSort(int arr[], int n) {
    int i, j;
    for (i = 0; i < n - 1; i++) { // it's n - 1, because index starts at 0, so its size - 1
        // Last i elements are already in place, so need to iterate over them
        for (j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                swap(&arr[j], &arr[j + 1]);
            }
        }
    }
}
~~~

### Insertion Sort

* Simple sorting algorithm, but not efficient.
* Starts at second element, and compares it with first element.
* If second is less than first, inserts it behind first, and first is now second, and second is now first.

From GeekSort:
To sort an array of size n in ascending order: 
1. Iterate from arr[1] (second element) to arr[n] (last element) over the array. 
2. Compare the current element (key) to its predecessor. 
3. If the key element is smaller than its predecessor, compare it to the elements before. Move the greater elements one position up to make space for the swapped element.

* The "compare to the elements before" in the third step is done by a while loop. So this algorithm uses a for loop and a while loop. The for loop iterates *only once*, and stops when it hits that `n + 1` is > `n`. Then the while loop kicks in.
* The while loop then basically swaps the misplaced element with the one behind it, and does that swap again and again, until the misplaced element is in the correct place.
  * When it does that swap, all the elements bigger than it, move up one place, which sorts them in the correct place.


~~~C++
void insertionSort(int arr[], int n) {
    int i, key, j;
    for (i = 1; i < n; i++) {
        key = arr[i];
        j = i - 1;

        /* Move elements of arr[0..i-1], that are greater than key, to one position ahead
        of their current position */
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}
~~~


![Insertion Sort Diagram](.media/insertion-sort.png)


### Greedy Algorithms
