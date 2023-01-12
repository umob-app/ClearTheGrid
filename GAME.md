# ClearTheGrid

You are given a grid, filled with numbers. 
You can move a number horizontally or vertically by exactly as many cells as the value of the number. The number has to be pushed on another non-zero number. The moved number will then be added to the other number or subtracted, at your choice. In case of substration, the absolute value will be taken. The goal is to *Clear-The-Grid* and not have any numbers remaining. 

## Example

We will use the first level as an example.
In this level the grid is 8x5 and contains: 

![board](Images/board1.png)

A first action to clear the grid could be to move the left 7 on top of the right 7 and substract it. This will leave us with the board: 

![board](Images/board2.png)

To get rid of the 3,1 and 2. One could move the 1 on top of the 3 and substract it. Resulting in :

![board](Images/board3.png)

To clear the grid, we move one of the 2's on top of the other. The grid is clear! 

![board](Images/board4.png)


## Details

The top left corner has the coordinate (0,0). The X coordinate increases to the right, the Y to the bottom.

### Input file
The level files consist of :
- On the first line the `width` and `height`
- The other *`height`* number of lines contain the `width` number of cell values of the grid.


For example the content of the first level defines a grid of 8 width and 5 height.
``` 
8 5
0 0 0 0 0 0 0 0 
7 0 0 0 0 0 0 7 
3 1 2 0 0 0 0 0 
0 0 0 0 0 0 0 0 
0 0 0 0 0 0 0 0 
```


### Solutions file

You can provide an solution to a level by constructing a file which contains 
- place each *move* on a line
- each line should contain 
   - the `x` and `y` coordinate of the source cell 
   - the direction as one of the uppercase letters [`U`, `D`, `L` or `R`] for the directions : up,down,left or right.
   - your choice for addition or subtraction by writing the `+` or `-` sign. 

A (free!) solution for the first level could be:

```
0 1 R -
1 2 L -
0 2 R -
```

> The first line reads as: take the cell at [0,1] (which is the left 7 in the grid) and move it's value to the right. Substract it from the other 7. This clears out both the 7's.

### Check 

In the source of this repo you find a `Checker` tool to verify if your generated solution file is correct. 


