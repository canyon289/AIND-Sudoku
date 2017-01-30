# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Naked Twins is another method through which possible digits can eliminated
as values for boxes. With this method when two boxes have the same two solutions
and are located in the same unit, or constraint space, this means that 
no other boxes besides can be these two values. Eliminating the 
conflicting digits from the non twin boxes is the constraint propogation.
Worded another way constraint propogation allows us to further cut down
the possible solution space for all boxes in a unit, given that two
boxes in the unit are constrained to the same two values.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: Diagonal Sudoku introduces another constraint, in that the diagonal boxes
now also cannot share the same digit as another box in the same diagonal.
This constraint is added by adding two more units to our unitlist. When
solving the puzzle the constraint propogation is handled identically to the 
normal row, box, and square, constraint. If any of the boxes in the diagonals
have a known value, that value constrains the possible solution digits of
all the other boxes. By removing the solved digit from all other diagonals
we are using constraint propogation to narrow down the possible solutions 
repeatedly until the final solution is obtained.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.
