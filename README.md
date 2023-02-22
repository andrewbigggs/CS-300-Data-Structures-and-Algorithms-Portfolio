# CS-300-Data-Structures-and-Algorithms-Portfolio

The problem I solved for the projects in this course was to take a comma separated values (CSV) file and import the data. 
The CSV file is to contain data about courses, with the courseNumber, courseName, prereq1, prereq2, prereq3 as the values.
This was done by importing the data and adding it to a binary search tree. Since the CSV file was small, I didn't include
additional logic to minimize the tree height, but such a function will be easy to add in a future implementation.

I approached the problem with the understanding that the stored data would likely need to be searched often. I thought
about different ways a data structure containing information about school courses would be used and concluded that a
data structure that would minimize search times for specific courses is best. This is why I went with a binary search
tree. Binary Search Tree also has the added benefit of alphanumerically sorting the data as it's built just because of
the nature of how this data structure is implemented.

One of the biggest roadblocks in developing this was deciding to use a vector over an array. Initially, I wanted to use
an array to store the values from the CSV file as they were loaded into the program, but found that it's impossible to
return an array from a function and that it's also much easier to append to a vector using the .push_back(x) function.
Ultimately, I think a more efficient implementation of this program will involve arrays instead of vectors, but at the
cost of less-readable and less-maintainable code (since an array must be copied and resized in the case, for example, that
a future implementation would involve many more values per line of the CSV file.)

This course has deepened my understanding of space and time complexities, and given me a peek at how different data
structures stack up against one another according to their complexities. For tiny operations like the ones intended by this
program, the differences in efficiency are minute. As the running program as a whole, grows more elaborate, however, 
and the number of iterations extends ever higher, ever smaller gains in efficiency in time and space usage become more
important.

My code has become more readable and I've honed my ability to write concise and clear inline and block comments, which are
crucial to readability of code. Most of my test harnesses involved std::cout statements, but I found myself looking for
good places to implement try-throw-catch blocks as these help make code more maintainable since the tests are built in.
