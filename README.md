SESSION-1 ASSIGNMENT 1
1. Say True or False for the below statements:
• Prescriptive Analytics used to predict the future outcomes?
 False
• Base R packages installed automatically?
True
2. What is Recycling of elements in a vector?
Recycling occurs when vector arithmetic is performed on multiple vectors of different sizes. R takes the shorter vector and repeats them until it becomes long enough to match the longer one.
When applying an operation to two vectors that requires them to be the same length, R automatically recycles, or repeats, elements of the shorter one, until it is long enough to match the longer Vector. 
Example 1:
Suppose we have two Vectors c(1,2,4) , c(6,0,9,10,13), where the first one is shorter with only 3 elements. Now if we sum these two, we will get a warning message as follows.
> c(1,2,4) + c(6,0,9,10,13)
[1]  7  2 13 11 15
Warning message:
In c(1, 2, 4) + c(6, 0, 9, 10, 13) :  longer object length is not a multiple of shorter object length

Here R Sum those Vectors by Recycling or repeating the elements in shorter one, until it is long enough to match the longer one as follows..

> c(1,2,4,1,2) + c(6,0,9,10,13)
[1] 7 2 13 11 15
3. Give an example of recycling of elements.
> x[1] 3 6 8
> y[1] 2 9 0
> x + y[1]  5 15  8
> x + 1    # 1 is recycled to (1,1,1)
[1] 4 7 9
> x + c(1,4)    # (1,4) is recycled to (1,4,1) but warning issued
[1]  4 10  9
Warning message:
In x + c(1, 4) :longer object length is not a multiple of shorter object length
