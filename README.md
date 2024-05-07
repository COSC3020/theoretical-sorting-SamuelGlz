[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.


To test this theoretical sorting algorithm I would run a lot of randomly generated tests, like the ones we have been doing in our test files, and plotting out the time for completion on the y axis and the size of the given array in the x axis (like the suggestion in tsp comparison). Trying to get a good representation in the plot for differing sizes of inputs.

If the algorithm can indeed sort in O(n) time I would expect to see a linear growth as the size of the array increases. In the same graph I would overlay the time that a quicksort implementation took for the same array, this would be useful as a point of comparison for larger sizes or arrays as a theoretical sorting algorithm O(n) would have an smaller average run time (the average of the run time for multiple arrays of size n) than the quicksort O(nlog(n)) for large input sizes. I would also make sure to test for some of the common edge cases like: an already sorted algorithm or list sorted in decending order. I would also try to running this in multiple computers, to account for any possible machine differences. 


With the thoery that we covered in class and in the slides this type of sorting algorithm should not be possible. We can represent a comparison sorting based algorithm with a decision tree that has n! leaves and has a height of is nlog(n). This means that any algorithm that depends on comparing values two at a time will have at least a worst case scenario of log(n!) = n*log(n), which is not compatible with the given O(n).
