Download Link: https://assignmentchef.com/product/solved-coen12-project-2-sets-and-arrays
<br>
In this project, you will implement a set abstract data type for strings. Your interface and implementation must be kept separate. Separate source files that provide main will be provided for testing your data type.

<h1>1        Interface</h1>

The interface to your abstract data type must provide the following operations:

<ul>

 <li>SET *createSet(int maxElts); return a pointer to a new set with a maximum capacity of <em>maxElts</em></li>

 <li>void destroySet(SET *sp); deallocate memory associated with the set pointed to by <em>sp</em></li>

 <li>int numElements(SET *sp); return the number of elements in the set pointed to by <em>sp</em></li>

 <li>void addElement(SET *sp, char *elt); add <em>elt </em>to the set pointed to by <em>sp</em></li>

 <li>void removeElement(SET *sp, char *elt); remove <em>elt </em>from the set pointed to by <em>sp</em></li>

 <li>char *findElement(SET *sp, char *elt); if <em>elt </em>is present in the set pointed to by <em>sp </em>then return the matching element, otherwise return NULL</li>

 <li>char **getElements(SET *sp); allocate and return an array of elements in the set pointed to by <em>sp</em></li>

</ul>

<h1>2        Implementation</h1>

You will write two different implementations of the data type for this assignment. First, implement a set using an unsorted array of length <em>m &gt; </em>0, in which the first <em>n ≤m </em>slots are used to hold <em>n </em>strings in some arbitrary order. Use sequential search to locate an element in the array. Second, implement a set using a sorted array of length <em>m &gt; </em>0, in which the first <em>n ≤m </em>slots are used to hold <em>n </em>strings in ascending order. Use binary search to locate an element in the array.

Forbothimplementations, ratherthanduplicatingthesearchlogicinseveralfunctions, writeanauxiliaryfunction search that returns the location of an element in an array. Declare search as static so it is not visible outside the source file. Use search to implement the functions in the interface. Your implementation should allocate memory and copy the string when adding, and therefore also deallocate memory when removing.

By the end of the first lab, you should have finished the first implementation. You should verify that the ADT works with both test programs (unique, and then parity) on all of the files. Note that unique takes an optional second file, whose words it <strong><em>removes </em></strong>from the set, thus allowing you to test insertion followed by deletion. In contrast, parity interweaves insertion and deletion, so it is a tougher test. By the end of the second lab, you should have finished both implementations. Before the due date, make sure you finish commenting and testing your code. You should use the assert macro defined in &lt;assert.h&gt; where appropriate