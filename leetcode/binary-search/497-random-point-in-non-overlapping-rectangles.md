### Question {#question}

[https://leetcode.com/problems/random-point-in-non-overlapping-rectangles/description/](https://leetcode.com/problems/random-point-in-non-overlapping-rectangles/description/)

Given a list of non-overlapping axis-aligned rectangles rects, write a function pick which randomly and uniformily picks an integer point in the space covered by the rectangles.

**Note:    
**

1. An integer point is a point that has integer coordinates. 
2. A point on the perimeter of a rectangle is included in the space covered by the rectangles. 
3. ith rectangle = rects\[i\] = \[x1,y1,x2,y2\], where \[x1, y1\] are the integer coordinates of the bottom-left corner, and \[x2, y2\] are the integer coordinates of the top-right corner.
4. length and width of each rectangle does not exceed 2000.
5. 1 &lt;= rects.length &lt;= 100
6. pick return a point as an array of integer coordinates \[p\_x, p\_y\]
7. pick is called at most 10000 times.

**Example 1:**

```
Input: 
["Solution","pick","pick","pick"]
[[[[1,1,5,5]]],[],[],[]]
Output: 
[null,[4,1],[4,1],[3,3]]
```

**Example 2:**

```
Input: 
["Solution","pick","pick","pick","pick","pick"]
[[[[-2,-2,-1,-1],[1,0,3,0]]],[],[],[],[],[]]
Output: 
[null,[-1,-2],[2,0],[-2,-1],[3,0],[-2,-2]]
```

**Explanation of Input Syntax:  **

The input is two lists: the subroutines called and their arguments. Solution's constructor has one argument, the array of rectangles rects. pick has no arguments. Arguments are always wrapped with a list, even if there aren't any.

### Thought Process {#thought-process}

1. Binary Search
   1. Since the rectangles are non-overlapping, we can use each rectangle's area divided by total as probability of being picked
   2. We generate a random number, r, in the range of \[0, totalArea\)
   3. Then r is used to find out which rectangle is picked through process of binary search through accumulated area array
   4. After locating the rectangle, we can easily generate random point in this rectangle
   5. Time complexity O\(n\), where n is number of rectangles
   6. Space complexity O\(n\)
2. asd

### Solution

```java

```

### Additional {#additional}


