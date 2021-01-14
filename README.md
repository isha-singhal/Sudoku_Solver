# Week2-project
## SUDOKU SOLVER
In this project, I implemented a C++ program that solves Sudoku puzzles.
Sudoku is a logic puzzle. The objective is to fill a 9×9 grid with digits in such a way such that each column, each row, and each of the nine 3×3 grids that make up the larger 9×9 grid contains all of the digits from 1 to 9 exactly once.
Each Sudoku puzzle begins with some cells filled in. These numbers are chosen such that there is a unique solution to the Sudoku.
We go cell by cell instead of row by row. That is, “try every possible number for the next empty cell. If you find a solution with the current number, stop. If you don't, then try the next number.” Try to fill all the other empty cells in the similar manner recursively.If all the cells get filled without any conflict then simply return the solved Sudoku.
#### PROGRAMMING LANGUAGE USED: C++
#### PLATFORM USED: CODEBLOCKS
#### TECHNOLOGIES USED: Backtracking Approach
#### MODULES:
* bool isValid(int grid[N][N], int row, int col, int number) - checks whether or not it is valid to place number in the given position. That is, number should not appear in the   row, column, or grid.
* bool findUnassignedLocation(int grid[N][N], int &row, int &col) - finds the first unassigned or empty cell in the sudoku grid. row and column are passed by reference
* void displayGrid(int grid[N][N]) - displays the grid
* bool usedInRow(int grid[N][N], int row, int number) - returns whether or not "number" has been used in particular row.
* bool usedInCol(int grid[N][N], int col, int number) - returns whether or not "number" has been used in particular column.
* bool usedInSubgrid(int grid[N][N], int row, int col, int number) - returns whether or not "number" has been used in particular subgrid.
* bool solveSudoku(int grid[N][N]) - this is the main sudoku solver function which takes a partially filled-in grid and attempts to assign values to all unassigned locations in 
  such a way to meet the requirements for Sudoku solution (non-duplication across rows,columns, and subgrids).
