# projects
personal portfolio
    Imports: The program starts by importing necessary modules - pygame for creating the graphical interface, math for mathematical operations, and PriorityQueue from queue module for the A* algorithm.

    Constants: Define constants for the window width, the window itself (WIN), and color constants used throughout the program.

    Spot Class: Defines the Spot class which represents each grid cell. It includes methods to set and retrieve properties of the spot, such as its position, color, and whether it's a start, end, barrier, etc.

    Helper Functions:
        h(p1, p2): Calculates the heuristic function for A* algorithm, which is the Manhattan distance between two points.
        reconstruct_path(came_from, current, draw): Backtracks from the end spot to the start spot using the came_from dictionary and marks the path.
        algorithm(draw, grid, start, end): Implements the A* algorithm. It iteratively evaluates nodes based on their current path cost and heuristic cost to find the shortest path from start to end.

    Grid Creation Functions:
        make_grid(rows, width): Creates a 2D list representing the grid of spots.
        draw_grid(win, rows, width): Draws grid lines on the window.

    Main Function (main(win, width)):
        Initializes the grid and necessary variables.
        Enters the main loop where it listens for user input and updates the display accordingly.
        Event handling:
            pygame.QUIT: Quits the program if the window close button is clicked.
            Left Mouse Button Press: Sets the start, end, or barrier spots based on the user's click.
            Right Mouse Button Press: Resets the spot to empty if it was previously set as start/end, or removes barrier.
            pygame.KEYDOWN: Triggers different actions based on the key pressed. Pressing the spacebar (pygame.K_SPACE) starts the A* algorithm, while pressing 'c' (pygame.K_c) clears the grid.
        Finally, the program quits pygame when the main loop ends.

Overall, this program creates a graphical interface using pygame where users can interactively set start, end, and barrier spots on a grid, and then find the shortest path between the start and end spots using the A* algorithm.
