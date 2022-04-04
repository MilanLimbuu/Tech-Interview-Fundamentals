# Searching in Data Structure – Different Search Methods Explained

Introduction
In today’s world, the communication network is expanding at a very fast rate. Businesses are going digital to improve management efficiency. The amount of data generated on the internet is increasing, and as a result, datasets are becoming more complex. It is important to organize, manage, access, and analyze the data carefully and efficiently, a data structure is the most helpful method, and the article focuses on it

Data Structure
In computer science, data structures serve as the foundation for abstract data types (ADT), where ADT is the logical form of data types. The physical design of data types is implemented using data structures. various types of data structures are used for different types of applications; some are specialized in specific tasks.

Data structures are referred to as a collection of data values and relationships between them, functions, and operations applicable to the data. so that, users can easily access and modify the data efficiently.

Data structures help us to manage large amounts of data, such as huge databases. Efficient data structures are the fundamental basis for efficient algorithms. Besides efficient storage, data structures are also responsible for the efficient retrieval of data from stored locations. It includes an array, Graph, Searching, Programs, Linked List, Pointer, Stack, Queue, Structure, Sorting, and so forth.

The concepts of searching in a data structure, as well as its methods, are covered in this article.

## What is Searching in Data Structure?
Searching in data structure refers to the process of finding the required information from a collection of items stored as elements in the computer memory. These sets of items are in different forms, such as an array, linked list, graph, or tree. Another way to define searching in the data structures is by locating the desired element of specific characteristics in a collection of items.

Searching Methods
Searching in the data structure can be done by applying searching algorithms to check for or extract an element from any form of stored data structure.

These algorithms are classified according to the type of search operation they perform, such as:

Sequential search
The list or array of elements is traversed sequentially while checking every component of the set.
For example – Linear Search.

Interval Search
The interval search includes algorithms that are explicitly designed for searching in sorted data structures. In terms of efficiency, these algorithms are far better than linear search algorithms.
Example- Logarithmic Search, Binary search.

 
These methods are evaluated based on the time taken by an algorithm to search an element matching the search item in the data collections and are given by,

The best possible time
The average time
The worst-case time
The primary concerns are with worst-case times, which provide guaranteed predictions of the algorithm’s performance and are also easier to calculate than average times.

To illustrate concepts and examples in this article, we are assuming ‘n’ items in the data collection in any data format. To make analysis and algorithm comparison easier, dominant operations are used. A comparison is a dominant operation for searching in a data structure, denoted by O() and pronounced as “big-Oh” or “Oh.”

There are numerous searching algorithms in a data structure such as linear search, binary search, interpolation search, sublist search, exponential search, jump search, Fibonacci search, the ubiquitous binary search, recursive function for substring search, unbounded, binary search, and recursive program to search an element linearly in the given array. The article includes linear search, binary search, and interpolation search algorithms and their working principles.

Let’s take a closer look at the linear and binary searches in the data structure.

 

Linear Search
The linear search algorithm iteratively searches all elements of the array. It has the best execution time of one and the worst execution time of n, where n is the total number of items in the search array.

It is the simplest search algorithm in data structure and checks each item in the set of elements until it matches the searched element till the end of data collection. When the given data is unsorted, a linear search algorithm is preferred over other search algorithms.

Complexities in linear search are given below:

Space Complexity:

Since linear search uses no extra space, its space complexity is O(n), where n is the number of elements in an array.

Time Complexity:

Best-case complexity = O(1) occurs when the searched item is present at the first element in the search array.
Worst-case complexity = O(n) occurs when the required element is at the tail of the array or not present at all.
Average- case complexity = average case occurs when the item to be searched is in somewhere middle of the Array.
 

Pseudocode for the linear search algorithm

procedure linear_search (list, value)

   for each item in the list
      if match item == value
         return the item's location
      end if
   end for

end procedure
Example,

Let’s take the following array of elements:
45, 78, 15, 67, 08, 29, 39, 40, 12, 99
To find ‘29’ in an array of 10 elements given above, as we know linear search algorithm will check each element sequentially till its pointer points to 29 in the memory space. It takes O(6) time to find 29 in an array. To find 15, in the above array, it takes O(3), whereas, for 39, it requires O(7) time.
Binary Search
This algorithm locates specific items by comparing the middlemost items in the data collection. When a match is found, it returns the index of the item. When the middle item is greater than the search item, it looks for a central item of the left sub-array. If, on the other hand, the middle item is smaller than the search item, it explores for the middle item in the right sub-array. It keeps looking for an item until it finds it or the size of the sub-arrays reaches zero.

Binary search needs sorted order of items of the array. It works faster than a linear search algorithm. The binary search uses the divide and conquers principle.

Run-time complexity = O(log n)

Complexities in binary search are given below:

The worst-case complexity in binary search is O(n log n).
The average case complexity in binary search is O(n log n)
Best case complexity = O (1)
Pseudocode for the Binary search algorithm

Procedure binary_search
   A ← sorted array
   n ← size of array
   x ← value to be searched

   Set lowerBound = 1
   Set upperBound = n 

   while x not found
      if upperBound < lowerBound 
         EXIT: x does not exists.
   
      set midPoint = lowerBound + ( upperBound - lowerBound ) / 2
      
      if A[midPoint]  x
         set upperBound = midPoint - 1 

      if A[midPoint] = x 
         EXIT: x found at location midPoint
   end while
   
end procedure
Example,

Let’s take a sorted array of 08 elements:
09, 12, 26, 39, 45, 61, 67, 78
To find 61 in an array of the above elements,
The algorithm will divide an array into two arrays, 09, 12, 26, 39 and 45, 61, 67, 78
As 61 is greater than 39, it will start searching for elements on the right side of the array.
It will further divide the into two such as 45, 61 and 67, 78
As 61 is smaller than 67, it will start searching on the left of that sub-array.
That subarray is again divided into two as 45 and 61.
As 61 is the number matching to the search element, it will return the index number of that element in the array.
It will conclude that the search element 61 is located at the 6th position in an array.
Binary search reduces the time to half as the comparison count is reduced significantly as compared to the linear search algorithm.

Interpolation Search
It’s a better version of the binary search algorithm that focuses on the probing position of the search element. It only works on sorted data collection, similar to binary search algorithms.

Complexities in interpolation search are given below:

When the middle (our approximation) is the desired key, Interpolation Search works best. As a result, the best case time complexity is O(1).

If the data set is sorted and distributed uniformly, the interpolation search’s average time complexity is O(log2(log2n)), where n denotes the total of elements in an array.

In the worst-case scenario, we’ll have to traverse the entire array, which will take O(n) time.

An interpolation search is used when the location of the target element is known in the data collection. If you want to find Rahul’s phone number in the phone book, instead of using a linear or binary search, you can directly probe to memory space storage where names begin with ‘R’.

Pseudocode for the Interpolation search algorithm

A → Array list
N → Size of A
X → Target Value

Procedure Interpolation_Search()

   Set Lo  →  0
   Set Mid → -1
   Set Hi  →  N-1

   While X does not match
   
      if Lo equals to Hi OR A[Lo] equals to A[Hi]
         EXIT: Failure, Target not found
      end if
      
      Set Mid = Lo + ((Hi - Lo) / (A[Hi] - A[Lo])) * (X - A[Lo]) 

      if A[Mid] = X
         EXIT: Success, Target found at Mid
      else 
         if A[Mid]  X
            Set Hi to Mid-1
         end if
      end if
   End While

End Procedure
Conclusion
Finding a given element in an array of ‘n’ elements is referred to as searching in data structures. In searching, there are two types: sequential search and interval search. Almost every search algorithm falls into one of these two categories. Linear and binary searches are two simple and easy-to-implement algorithms, with binary algorithms performing faster than linear algorithms.

Though linear search is the most basic, it checks each element until it finds a match to the search element, making it efficient when data collection is not properly sorted. However, binary search is faster if the data collection is sorted and the length of an array is large.

When dealing with datasets, the data structure is an essential part of computer programming. Programmers and developers must constantly update and improve their skills in computer programming techniques.
