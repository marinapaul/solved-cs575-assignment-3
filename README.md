Download Link: https://assignmentchef.com/product/solved-cs575-assignment-3
<br>
<strong><u>Objective: </u></strong>

<ul>

 <li>Design and analyze an algorithm using dynamic programming strategy</li>

 <li>Enhance the concept of heap for sorting.</li>

</ul>

There are two parts in this assignment: (A) Theory part and (B) programming part

<strong><u>[Part A] Theory</u></strong>

<ol>

 <li>Given the following array:</li>

</ol>

<ol>

 <li style="list-style-type: none;">

  <ol>

   <li> Show the essential complete binary tree for the following array:</li>

  </ol></li>

</ol>

<table>

 <tbody>

  <tr>

   <td width="59">11</td>

   <td width="59">4</td>

   <td width="59">6</td>

   <td width="59">15</td>

   <td width="59">9</td>

   <td width="59">16</td>

   <td width="59">2</td>

   <td width="59">25</td>

   <td width="59">7</td>

   <td width="59">5</td>

  </tr>

 </tbody>

</table>




<ol>

 <li style="list-style-type: none;">

  <ol>

   <li> Convert the essential complete binary tree into a min heap using the fast-make-heap method. Draw the essential complete binary tree after each <em>siftDown</em>.</li>

   <li> Using the max-heap sorting algorithm to sort the above sequence in the non-decreasing order. Show the heap after the value “9” has been moved to the sorted sequence.</li>

  </ol></li>

</ol>




<ol start="2">

 <li> Find the longest common subsequence for the strings S=α β α µ £ α α  β, and T = £ µ α µ β µ £ £ α µ β. Show the table with the lengths and arrows.</li>

 <li>Find the shortest distance between all pairs of nodes in the following graph. Show the matrices <em>D</em><sup>0</sup>, <em>D</em><sup>1</sup>, …, <em>D</em><sup>4 </sup>and <em>P</em><sup>0</sup>, <em>P</em><sup>1</sup>, …, <em>P</em><sup>4</sup></li>

</ol>

(4)  Does Floyd’s algorithm always yield correct results? Use following graph to justify your answer.

<ol start="5">

 <li> If we want to design an algorithm to merge two heaps of sizes <em>n</em>1 and <em>n</em>2. Assume that heap 1 is stored in bt1[1,…,n1] and heap 2 is stored in bt2[1,…,n2]. Assume that n2 &gt;= n1. The two heaps do not overlap.</li>

</ol>

Is the following solution correct?

If yes, give the upper bound of the time complexity.

If not, give an example where it is wrong, describe a correct solution, and give the upper bound of the time complexity.

Copy the larger heap at the end of the smaller one. After the copy bt1 contains all n1 + n2 values. Now apply siftDown to all tree nodes from n1 down to 1.

<strong>for</strong> (i=1; i &lt;=n2, i++)

bt1[n1+i] = bt2[i]

last = n1 + n2

<strong>for</strong> (i=n1; i &gt; 0, i=i-1)

siftDown(bt1, i)




<ol>

 <li>[6%] Compute the binomial value of  using dynamic programming B table. [4%] Can you make a small B table (less than 6 columns) to obtain the solution.</li>

</ol>




<ol>

 <li> [12%]</li>

</ol>

Design a dynamic programming algorithm to solve the sum of subsets problem:




There are <em>n</em> positive integers,  and a positive integer sum <em>S</em>.  Is there a subset <em>A</em> of the <em>n</em> integers such that the sum of the integers in the subset is S, ()? If there is such a subset the output of the program is <em>true</em> otherwise it is <em>false</em>.




Example:  In this case the output is <em>true</em> since <em>p</em><sub>2</sub>+ <em>p</em><sub>3</sub> = 16.

Example:  In this case there is no solution, and the output is <em>false</em>.




The problem can be solved with dynamic programming.

A <strong>Boolean</strong> matrix <em>B</em> with rows 0 to <em>n</em> and columns 0 to <em>S</em> is generated. For the examples above the matrix has rows 0 to 3, and columns 0 to 16.

<em>B</em>[<em>i</em>, <em>s</em>] is <strong>true</strong> if a subset of the first <em>i</em> integers sums to <em>s</em>, otherwise it is <strong>false</strong>.

The solution to the original problem is <strong>true</strong> if <em>B</em>[<em>n</em>, <em>S</em>]= <strong>true</strong>, otherwise it is <strong>false.</strong>

(1) [5%] Write the recurrence relation for the solution.

<ul>

 <li>[4%] Write pseudo code to compute B.</li>

 <li>[3%] Apply dynamic programming to the following problem:  Show your matrix B.  Each element of B has the value <em>true</em> or <em>false</em>. Also, use arrows to show the matrix elements that were ordered, or used.</li>

</ul>

<ol start="8">

 <li>(5%) Show that the number of distinct binary search tree b(n) that can be constructed for a set of n orderable keys satisfies the recurrence relation:</li>

</ol>

<strong><u> </u></strong>

<strong> </strong>

<ol start="9">

 <li>(5%) Constructing the optimal binary search tree, given</li>

</ol>

<strong><u> </u></strong>




Show the dynamic programming tables of each step.

<strong><u> </u></strong>




<ol start="10">

 <li>(Optional: Extra points 10%)</li>

</ol>




Suppose there is an apartment available for rent for a year. There are 6 requesters who want to rent the apartment for 6 different periods of time with 6 different offers:




Requester 1:  starting January 1<sup>st</sup> for 3 months, and would like to pay $2k;

Requester 2:  starting February 1<sup>st</sup> for 5 months, and would like to pay $4k;

Requester 3:  starting May 1<sup>st</sup> for 5 months, and would like to pay $4k;

Requester 4:  starting April 1<sup>st</sup> for 7 months, and would like to pay $7k;

Requester 5:  starting October 1<sup>st</sup> for 2 months, and would like to pay $2k;

Requester 6:  starting November 1<sup>st</sup> for 2 months, and would like to pay $1k;




Since the apartment cannot be rented for more than one requester at a same period of time, design a dynamic programming algorithm to select the subset of requesters in order to maximize the sum of rentals (values).




<ul>

 <li>Write the recurrence relation for the solution;</li>

 <li>Show the time complexity of your algorithm;</li>

 <li>Using the above instance, show the dynamic programming table of your solution from the 6 requesters;</li>

</ul>




(Hint: The problem can be generalized by <em>j </em>requesters (j=1, 2, …, n), and each requester would like to pay <em>v(j)</em> dollars for <em>t(j)</em> period of time. )

<strong> </strong>

<strong><u>[Part B] Programming </u></strong>




<ol>

 <li>[18%] Given a following map, find the shortest path from New York City to Toronto using the dynamic programming approach. (The numbers shown on the map are the distances in miles between cities).</li>

</ol>




<ol start="2">

 <li>(10%) Find the longest common sequence of two strings by the dynamic programming algorithm. Test your implementation with the following two strings: 6541254939322816220209974565477289648317, 3142522751761601737419090933147067701840</li>

</ol>

Output:  length of LCS and the actual LCS.

<ol start="3">

 <li>(Optional: Extra 10%) Design a three-string LCS algorithm for finding the longest common subsequence (LCS) of three strings. Indicate the time complexity of your algorithm. Test your algorithm using following three strings:</li>

</ol>




String 1: 6541254939322816220209974565477289648317

String 2: 3142522751761601737419090933147067701840

String 3: 2807030561290354259513570160162463275171







<strong>Output: length of LCS and the actual LCS </strong>




Hint:

<ol>

 <li>Extend the recurrence equation from two strings to three strings (e.g., length-LCS(i, j, k)).</li>

</ol>







<u>Note 1:</u>







For Part B, submit one zip file of your code package including your code, makefile, and write-up (.doc).  The title is:

firstname_lastname_programming_language_used.tar.gz orfirstname_lastname_programming_language_used.zip