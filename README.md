# pyraminx_astar
This program is a Python implementation of a Pyraminx solver with a GUI. We represent the Pyraminx as a set of four faces: front (F), right ®, left (L), and down (D). Each face is stored as a 2D list with their respective colors represented by letters of Y, R, B, or G. For the GUI, we use tkinter to create a window with a canvas for displaying the Pyraminx. This window displays the moves as they are found from the A* algorithm. It is important to note that the program may say that the “GUI is not responding” once it reaches a certain k value. However, this is not a problem but rather just the program dealing with the exponential growth of the algorithm. Once the next move is found, the GUI will update again - it might just take a minute or two depending on the processing speed of the computer it is being run on. For the moves, we have clockwise (for scrambling) and counterclockwise (for solving). The moves are represented as methods that manipulate the data structures of the faces. For scrambling the puzzle, we have a scramble method that picks a random move and applies it to the puzzle. The number of random moves is specified by a loop that runs through 3-20. As for solving, we implement the iterative A* search algorithm to find a solution. We also implement a depth-limited A* algorithm to manage the search space. Furthermore, we use a heuristic function based on the maximum number of distinct colors on any one face in order to give the A* algorithm information to build off of. In order to run the needed number of iterations for this project (k=3-20 iterations, with 5 puzzles each), we implement a function to run that. The experiments function scrambles the Pyraminx based on what iteration it’s on, runs that specified number of scrambles for 5 different puzzles, solves each scrambled state and records the number of moves in the solution and nodes expanded during the search. In this, we also record the average number of nodes expanded in each iteration. For the plot aspect of this project, we use matplotlib to plot the average number of nodes expanded against the number of moves in the scramble. Lastly, our main execution creates the GUI window and Pyraminx object, and runs the experiments. To summarize, this program combines the A* solver algorithm, an experimental analysis, and a GUI in order to showcase the A* solver for the Pyraminx puzzle. 
