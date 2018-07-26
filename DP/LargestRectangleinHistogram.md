Given n non-negative integers representing the histogram's bar height where the width of each bar is 1, find the area of largest rectangle in the histogram.


Above is a histogram where width of each bar is 1, given height = [2,1,5,6,2,3].

![](histogram.png) 


The largest rectangle is shown in the shaded area, which has area = 10 unit.

![](histogram_area.png)
 

Example:

Input: [2,1,5,6,2,3]
Output: 10


This problem is similar to MaximumRectangle problem.

Method 1:
Brute force O(n2)
With every bar as starting point and calculate the maximal rectangle

Method 2:
Calculate the area of each bar as the minimum height;
Using stack to keep track of the bars.

