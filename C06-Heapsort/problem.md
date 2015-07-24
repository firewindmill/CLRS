### Problems 1 : Building a heap using insertion
***
The procedure BUILD-MAX-HEAP in Section 6.3 can be implemented by repeatedly using MAX-HEAP-INSERT to insert the elements into the heap. Consider the following implementation:

	BUILD-MAX-HEAP'(A)

a. Do the procedures BUILD-MAX-HEAP and BUILD-MAX-HEAP' always create the same heap when run on the same input array? Prove that they do, or provide a counterexample.
b. Show that in the worst case, BUILD-MAX-HEAP' requires Θ(n lg n) time to build an n-element heap.

### `Answer`
**a.**
不一定.对于数组[1,2,3,4,5,6].有

![](./repo/p/1.png)


**b.**
当原数组是递增序列时，需要的时间

![](http://latex.codecogs.com/gif.latex? T = \\sum_{i = 2}^{n}\\lg{i} = \\lg{n!} = \\Theta\(n\\lg{n}\) )



### Problems 2 : Analysis of d-ary heaps
***
A d-ary heap is like a binary heap, but (with one possible exception) non-leaf nodes have d children instead of 2 children.

### `Answer`
[implementation](./d-ary-heaps.cpp)

![](http://latex.codecogs.com/gif.latex? \\quad\\text{Height :} \\log_{d}{n} )

![](http://latex.codecogs.com/gif.latex? \\quad\\text{\\textbf{Complexity}} \\\\
\\quad\\text{ EXTRACT-MAX : } d\\log_{d}{n} \\\\
\\quad\\text{ INSERT : } \\log_{d}{n} \\\\ 
\\quad\\text{ INCREASE-KEY : } \\log_{d}{n} )


### Problems 3 : Young tableaus
***
An m × n Young tableau is an m × n matrix such that the entries of each row are in sorted order from left to right and the entries of each column are in sorted order from top to bottom. Some of the entries of a Young tableau may be ∞, which we treat as nonexistent elements. Thus, a Young tableau can be used to hold r ≤ mn finite numbers.





![](http://latex.codecogs.com/gif.latex?



T(p) = T(p-1) + O(1) = O(p)

**d.**
跟c是一个相反的操作，具体见代码.

**e.**
![](http://latex.codecogs.com/gif.latex? 
T = n^2O\(p\)  = O\(n^3\))

**f.**
实现见代码.

 
***
Follow [@louis1992](https://github.com/gzc) on github to help finish this task.
