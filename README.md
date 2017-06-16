# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: We use Constraint Propagation in this assignment which is used to apply a given constraint to a problem repeatedly until a solution is obtained or till the constraint can no longer be used, thus resulting in failure. In this solution, the Naked Twins problem is addressed by first finding pairs of boxes having 2 possibilities within a given unit and then identifying if the boxes outlined have the same possibilities (for ex: If F3 and I3 in the image below have the same possible values as 23). If yes, then they are Naked Twins and the rest of the boxes within that unit should remove those given values thus further refining the solution.

![Naked Twins](https://github.com/rsdelhi91/AIND-Sudoku/raw/master/images/naked-twins.png)


# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: The Diagonal sudoku problem is quite straightforward to address - we take the diagonals as a separate unit on its own by looking at the indices to identify the relevant boxes and adding it to our list of units in the variable unitlist (Look at solution.py). Following this, we treat the diagonals as a normal unit and perform the same steps that would be conducted in any given unit formation on the board.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solution.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the `assign_value` function provided in solution.py

### Submission
Before submitting your solution to a reviewer, you are required to submit your project to Udacity's Project Assistant, which will provide some initial feedback.  

The setup is simple.  If you have not installed the client tool already, then you may do so with the command `pip install udacity-pa`.  

To submit your code to the project assistant, run `udacity submit` from within the top-level directory of this project.  You will be prompted for a username and password.  If you login using google or facebook, visit [this link](https://project-assistant.udacity.com/auth_tokens/jwt_login) for alternate login instructions.

This process will create a zipfile in your top-level directory named sudoku-<id>.zip.  This is the file that you should submit to the Udacity reviews system.

