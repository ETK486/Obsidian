	An array is a collection of items of the same variable type that are stored at contiguous memory locations. It’s one of the most popular and simple data structures and is often used to implement other data structures. Each item in an array is indexed starting with 0. We can directly access an array element by using its index value.
###### Basic terminologies of array 

- **Array Index:** In an array, elements are identified by their indexes. Array index starts from 0.
- **Array element:** Elements are items stored in an array and can be accessed by their index.
- **Array Length:** The length of an array is determined by the number of elements it can contain.
###### Representation of Array

	The representation of an array can be defined by its declaration. A declaration means allocating memory for an array of a given size.
![[Pasted image 20231104210110.png]]

###### Declaration  in C++:
	int arr[5];        // This array will store integer type element
	char arr[10];    // This array will store char type element
	float arr[20];  // This array will store float type element 

###### Types of arrays:

There are majorly two types of arrays:
- One-dimensional array (1-D arrays): You can imagine a 1d array as a row, where elements are stored one after another.
![[Pasted image 20231104210619.png]]
- Two-dimensional array (2-D arrays): Multidimensional array can be considered as an array of arrays or as a matrix consisting of rows and columns.
![[Pasted image 20231104210631.png]]
- Three-dimensional array: A 3-D multidimensional array contains three dimensions, so it can be considered an array of two-dimensional arrays.
![[Pasted image 20231104210642.png]]
######  Types of Array operations:

- Traversal: Traverse through the elements of an array.
- Insertion: Inserting a new element in an array.
- Deletion: Deleting element from the array.
- Searching:  Search for an element in the array.
- Sorting: Maintaining the order of elements in the array.

###### Advantages of using Arrays:

- Arrays allow random access to elements. This makes accessing elements by position faster.
- Arrays have better cache locality which makes a pretty big difference in performance.
- Arrays represent multiple data items of the same type using a single name.
- Arrays store multiple data of similar types with the same name.
- Array data structures are used to implement the other data structures like linked lists, stacks, queues, trees, graphs, etc.

###### Disadvantages of Array:

- As arrays have a fixed size, once the memory is allocated to them, it cannot be increased or decreased, making it impossible to store extra data if required. An array of fixed size is referred to as a static array. 
- Allocating less memory than required to an array leads to loss of data.  
- An array is homogeneous in nature so, a single array cannot store values of different data types. 
- Arrays store data in contiguous memory locations, which makes deletion and insertion very difficult to implement. This problem is overcome by implementing linked lists, which allow elements to be accessed sequentially.  

###### Application of Array:

- They are used in the implementation of other data structures such as array lists, heaps, hash tables, vectors, and matrices.
- Database records are usually implemented as arrays.
- It is used in lookup tables by computer.
- It is used for different sorting algorithms such as bubble sort insertion sort, merge sort, and quick sort.