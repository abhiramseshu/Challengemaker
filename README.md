Highway Navigation
------------------
Maxtern is driving a car on a 3-lane highway and needs to reach a destination at the end of the highway. The highway is represented by an N×3 matrix, where each cell can be either 0 or 1. The car can only move to a cell containing 0.

```
 -> 0 represents an open lane where the car can move.

 -> 1 represents a lane occupied by another car where movement is not allowed.

```

The car can move in the following directions:

```
->To the above cell.

->Right to the cell(if it exists).

->Left to the cell(if it exists).

->The movement only happens if there exists an empty road.

```

The goal is to determine if the car can reach the first row (destination) from the starting position in the middle lane of the last row.

**Input Format**

-   `An integer T,where T is the number of testcases.`
-   `An integer N ,where N is the number of rows in the matrix.`
-   `An 𝑁×3 matrix matrix where matrix[i][j] is either 0 or 1. The car always starts at matrix[0][1], which is guaranteed to be 0.`

**Constraints**

-   1 ≤ T ≤ 4
-   1 ≤ N ≤ 102
-   The input matrix will always have exactly 3 columns.
-   The matrix will have at least one row.

**Output Format**

Return True if it is possible for the car to reach the last row, else return False.

**Note**:

```
Last row for every input contains a 0 as car begins there.

```

**Sample Input 0**
- 1
- 4
- 0 0 0
- 1 1 0
- 1 0 0
- 1 0 1

**Sample Output 0**

True

**Explanation 0**

![image](https://s3.amazonaws.com/hr-assets/0/1723996590-4d60c27793-image.jpg)

**Sample Input 1**

- 2
- 4
- 0 0 1
- 1 0 1
- 1 0 0
- 0 0 1
- 5
- 1 1 1
- 0 0 0
- 0 1 0
- 1 0 1
- 0 0 0

**Sample Output 1**

- True
- False

**Explanation 1**

**Explanation Case-1:**

-   Starting from the bottom row, valid starting positions are (3, 0) and (3, 1).
-   From (3, 0), you can move to (2, 0) (blocked) or (3, 1) (open).
-   From (3, 1), you can move to (2, 1) (open).
-   From (2, 1), you can move to (1, 1) (open).
-   From (1, 1), you can move to (0, 1) (open).
-   From (0, 1), you can move up to the top row.

Thus, there is a valid path from the bottom to the top row.**(True)**

**Explanation Case-2:**

-   Starting from the bottom row, valid starting positions are (4, 0) and (4, 1).
-   From (4, 0), you can only move to (3, 0) (blocked).
-   From (4, 1), you can move to (3, 1) (open).
-   From (3, 1), you can move to (2, 1) (blocked), (3, 2) (blocked), or (3, 0) (blocked).
-   No valid paths are found from (4, 1).

Thus, there is no valid path from the bottom to the top row.**(False)**
