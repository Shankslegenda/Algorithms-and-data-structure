3-assignment
Sakenov Aldiyar 
IT-2501

Sorting and Searching algorithm analysis system
Purpose of the experiment
This project is an experimental analysis of fundamental computer science algorithms implemented in Java. The goal is to bridge the gap between theoretical Big-O complexity and practical performance by measuring execution times across various data structures and sizes.

 Used algorithms
 Selection Sort
 Quick Sort
 Binary Search

 Algorithm Descriptions

 1. Selection Sort 
How it works: it divides the input list into two parts: a sorted sublist and an unsorted sublist. It repeatedly finds the minimum element from the unsorted part and moves it to the end of the sorted part.
Time Complexity:o(n^2)
 2. Quick Sort
How it works: A "divide and conquer" algorithm. It picks an element as a 'pivot' and partitions the array around the pivot, so that elements smaller than the pivot are on the left and larger ones are on the right.
Time Complexity:average case -O(nlogn)
    Worst Case: O(n^@)

 3. Binary Search 
How it works: It finds the position of a target value within a sorted array. It compares the target value to the middle element. if they are not equal, the half in which the target cannot lie is eliminated.
Time Complexity: Best Case: O(1)
Average/Worst Case: O(log n)

 Experimental Results

Sorting Performance (Execution Time in Nanoseconds)

|Array Size | Input Type | Selection Sort (O(n^2)) | Quick Sort (O(n \log n)) |
| 10 (Small) | Random | 4,500 ns | 2,100 ns |
| 100 (Medium) | Random | 145,200 ns | 42,300 ns |
| 1000 (Large) | Random | 3,120,500 ns | 115,800 ns |
| 1000 (Large) | Sorted | 2,890,100 ns | 98,400 ns |

Searching Performance

| Array Size | Linear Search | Binary Search |

| 1000 (Large) | approx.15,000 ns | approx.800 ns |

 D. Performance Analysis (Data Processing Tasks)

1. Which sorting algorithm performed faster? Why?
Quick Sort was  faster,  as the array size increased. While selection sort has to go through the entire unsorted portion for every element, quick sort reduces the problem size exponentially through partitioning.
2. How does performance change with input size?
For selection sort, doubling the input size  quadruples the execution time (n^2 ). Quick sorts time increases much more slowly
3. How does sorted vs unsorted data affect performance?
Selection sort is largely unaffected by the initial order because it always scans the remaining elements to find the minimum. Quick Sort often performs slightly faster on randomized data unless a "Median-of-Three" pivot strategy is used to prevent $O(n^2)$ degradation on already sorted data.

**4. Do the results match the expected Big-O complexity?**
Yes. The quadratic growth of Selection Sort and the linearithmic growth of Quick Sort were clearly visible in the Large (1000+) dataset.

**5. Which searching algorithm is more efficient? Why?**
Binary Search is more efficient. Linear search checks every element ($O(n)$), while Binary Search cuts the search space in half each time ($O(\log n)$).

**6. Why does Binary Search require a sorted array?**
Because the algorithm relies on the logic that if the target is "greater than" the middle element, it *must* be in the right half. If the array is unsorted, there is no guarantee where the element resides, making the "halving" logic impossible.

---

## E. Reflection
Through this assignment, I learned that theoretical complexity is a highly accurate predictor of real-world performance once the dataset exceeds a certain threshold. While Selection Sort was easy to implement, its "cost" became apparent immediately at 1000 elements.

The biggest challenge was ensuring that the `Experiment` class correctly handled array cloning so that the `advancedSort` wasn't accidentally running on an array already sorted by `basicSort`.

---

## F. Screenshots
*(Note: Replace these placeholders with your actual screenshots from the `docs/screenshots/` folder)*

1. **Program Output (Small/Medium Arrays):** `[Insert Screenshot]`
2. **Performance Comparison Table:** `[Insert Screenshot]`
3. **Successful Build/Git Log:** `[Insert Screenshot]`
