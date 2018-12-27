# algorithmslearn 

[| Basic Algorithm Design and Data Structures](https://github.com/tristaaa/algorithmslearn#-basic-algorithm-design-and-data-structures)<br>
&ensp;&ensp;[- Incremental Algorithm Design](https://github.com/tristaaa/algorithmslearn#11-incremental-algorithm-design)<br>
&ensp;&ensp;[- Asymptotics and Divide-and-Conquer](https://github.com/tristaaa/algorithmslearn#12-asymptotics-and-divide-and-conquer)<br>
&ensp;&ensp;[- Binary Search and Mergesort](https://github.com/tristaaa/algorithmslearn#13-binary-search-and-mergesort)<br>
&ensp;&ensp;[- Introduction to Probability](https://github.com/tristaaa/algorithmslearn#14-introduction-to-probability)<br>
&ensp;&ensp;[- Quicksort](https://github.com/tristaaa/algorithmslearn#15-quicksort)<br>
&ensp;&ensp;[- Priority Queues](https://github.com/tristaaa/algorithmslearn#16-priority-queues)<br>
&ensp;&ensp;[- Binary Search Trees](https://github.com/tristaaa/algorithmslearn#17-binary-search-trees)<br>
&ensp;&ensp;[- Hashing](https://github.com/tristaaa/algorithmslearn#18-hashing)<br>
&ensp;&ensp;[- Homework1](https://github.com/tristaaa/algorithmslearn#19-homework1)<br>
[| Design Paradigms: Dynamic Programming and Greedy Algorithms](https://github.com/tristaaa/algorithmslearn#-design-paradigms-dynamic-programming-and-greedy-algorithms)<br>
[| Graph Algorithms: Traversals and Spanning Trees](https://github.com/tristaaa/algorithmslearn#-graph-algorithms-traversals-and-spanning-trees)<br>
[| Shortest Paths and NP-completeness](https://github.com/tristaaa/algorithmslearn#-shortest-paths-and-np-completeness)<br>



---
Most From Edx Course Named **Algorithm Design and Analysis** Taught by Sampath Kannan

## | Basic Algorithm Design and Data Structures
### 1.1 Incremental Algorithm Design
#### Why learn Algorithms
- reason about whether your logic is correct
- and how fast the algorithm is going to be before you actucally code it up in a program
- once we start thinking abstractly, we notice commonalities between many different problems

#### Algorithm Design
- Fundamental idea in algorithm design:
    - solve a problem on bigger datasets using your knowledge of how to solve it on smaller ones
- it's a top dowm view to take the big problem, do a bit of reduction and get to a slightly smaller problem and continue this way until you get to a really small problem
- it embodies the proof technique of Mathematical Induction
- Eg(top down): Towers of Hanoi
    - in a temple in Thailand, there are three pegs
    - one of the pegs contains 64 disks of decresing size(largest disk at the bottom)
    - the Buddhist monks try to move all the disks on one peg to another, say the third peg
    - Rules: can only move one disk at a time & can never put a bigger disk on the top of a smaller one

    - Solution: 
        - think recursively, if you want to solve the problem on 64 disks, let's reduce it to solving the problem on 63 disks
        - Move top n-1 disks from rod A to rod B
            - imagine moving 63 disks from the first pegs to the second peg using the way we figured out for sovling the problem on 63 disks
        - Move disk 1 from rod A to rod C
            - once we done that, move the largest disk from peg one to peg three
        - Move the n-1 disks from rod B to rod C
            - reuse the procedure of moving the 63 disks from peg one to peg two
- Eg(bottom up): Insertion Sort
    - ![insertion sort](https://github.com/tristaaa/algorithmslearn/blob/master/pics/insertion%20sort.png)
    - want to put the numbers in ascending order
    - at first, we have the array consisting of the numbers 5,2,4,6,1,3
    - we're gonna solve small problems and slowly increase the size of the problems
        - which is to sort every number to the left of the red line
        - initially, we put the red line just after the first number(of course, the left part is sorted)
        - then move the red line one step to the right, number 5,2 isn't in sorted order, and we can take the number 2 and move ot until it's in the right place
        - continue like this, take the number 4 and move it leftwards until it's in the right place, and so on
    - pseudocode:
    ```python
    insertion-sort A:
        for i <- 1 to length(A)
            J <- i
            while j>0 and A[j-1] > A[j]:
                swap A[j] and A[j-1]
                j <- j-1
    ```

#### Recurrence Relations
- How can we analyze the running time of an algorithm that is recursive
- tool: recurrence relations
- the running time of an algorithm is always expressed in terms of the length of the input: n
- T(n) = # operations required to solve a tower with n disks
- T(n-1) = # operations required to solve a tower with n-1 disks
- rewrite T(n) using T(n-1)
- Eg: Towers of Hanoi recurrence:
    - T(n) = 2T(n-1) + 1 ①
    - then expand this recurrence out through telescoping:
        - T(n-1) = 2T(n-2) + 1 ②
        - so T(n) = 4T(n-2) + 3
        - and T(n) = 8T(n-3) + 7
        - generalize: <img src="https://latex.codecogs.com/gif.latex?T(n)&space;=&space;2^kT(n-k)&space;&plus;&space;(2^k&space;-&space;1)" title="T(n) = 2^kT(n-k) + (2^k - 1)"/><br>
        - and T(1) = 1 (by substituding k using n-1)
        - so <img src="https://latex.codecogs.com/gif.latex?T(n)&space;=&space;2^n&space;-&space;1" title="T(n) = 2^n - 1"/><br>




### 1.2 Asymptotics and Divide-and-Conquer

### 1.3 Binary Search and Mergesort

### 1.4 Introduction to Probability

### 1.5 Quicksort

### 1.6 Priority Queues

### 1.7 Binary Search Trees

### 1.8 Hashing

### 1.9 Homework1




## | Design Paradigms: Dynamic Programming and Greedy Algorithms
### 2.1 
#### BI


 
## | Graph Algorithms: Traversals and Spanning Trees




## | Shortest Paths and NP-completeness
