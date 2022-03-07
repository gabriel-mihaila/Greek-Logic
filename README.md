# Greek-Logic
Greek Logic Game solved using first order logic.
## Code explanation
For the modeling of this game I used the arithmetic set and I declared a distinct list of Greek letters,
taking into account domain size (4 in this case). In order to be able to place the Greek letters on the playing field I have
built a grid function with two arites (x coordinates and on the game board) that can take as values ​​one of the
4 Greek liters mentioned in the "How to play" section. Later I defined the uniqueness of each cell (a cell
may have only one Greek letter at a time).
In order to apply the rules of the game on rows, columns and the two diagonals, I built two other functions,
next and prev, in order to be able to navigate more easily through the game board to the cells of interest. As you can see,
the two functions are circular to be able to take the remaining 3 cells to be checked regardless of position
grid current. For example, next (3) will be 0, and prev (0) will be 3.
We model each rule separately as follows:
- we rule that when we have a letter on a certain column we can no longer have the same letter on that
column (when x changes);
- we rule that when we have a letter on a certain line we can no longer have the same letter on that one
rand (when y changes);
- we put the additional rule if the cell is part of the main diagonal and has a certain letter, that letter
it can no longer appear on the main diagonal;
- we put the additional rule if the cell is part of the secondary diagonal and has a certain letter, that letter
it can no longer appear on the secondary diagonal.
Finally, we model the initial context. For example we have a letter Sigma on the grid (0,0), a letter Pi on the grid (0,1), a
letter Lambda on the grid (0,2), or letter Delta on the grid (0,3) and letter Delta on the grid (3,2).
## Interpretation of the result
![AI](https://i.pinimg.com/564x/04/8d/65/048d65858de37d23b0f036d40b339169.jpg)
