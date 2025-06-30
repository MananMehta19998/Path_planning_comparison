Thesis Project
Title
Comparative Analysis of A* and Dijkstra for Path Planning in Duckietown
Author
Manan Mehta
B.Sc. Robotics and Intelligent Systems, Constructor University
2025

Supervisor
Prof. Dr. Francesco Maurelli


Overview
This project compares static path planning algorithms in a simplified Duckietown environment. The focus is on evaluating different strategies for safe and optimal navigation using:

Dijkstra's Algorithm
A* with Manhattan Heuristic
A* with Euclidean Heuristic

The comparison is performed under two modes:

Safety-first: Avoid high-risk areas near obstacles
Optimality-first: Prioritize shortest raw cost path


 Objective
To evaluate the effectiveness of static path planners based on:

 Runtime
Memory Usage
Obstacle Avoidance
Path Cost
Search tree



 Methods
10x10 grid representing the Duckietown layout
Static obstacles manually placed
Risk zones modeled using smoothed Gaussian cost maps
Start: (0, 0)
Goal: (9, 9)

Each planner is executed in both safety-first and optimality-first modes, and logs/graphs are generated for comparison.


Outputs
Path Visualizations overlaid on map
Search Area Graphs showing number of nodes explored
Heatmaps showing proximity to obstacles
Comparison Logs with:
Runtime
Memory usage



 Project Structure
Duckietown-Thesis/

├── planning/

│   ├── dijkstra_safety.py

│   ├── dijkstra.py

│   ├── astar_manhattan_safety.py

│   ├── astar_euclidean.py

│   ├── astar_manhattan.py

│   └── astar_euclidean.py

├── simulation/

│   ├── simulate.py

│   └── simulate_safety.py

├── results/

│   └── *.png (paths, heatmaps, search graphs)

├── logs/

│   └── *.txt (runtime, memory)

├── data/

│   └── duckietown_layout.png

├── README.md

└── requirements.txt


Running the Simulation
Optimality-First Planning
python integration/simulate.py
Safety-First Planning
python integration/simulate_safety.py


Python Libraries Used
Standard Libraries: heapq, time, tracemalloc, math
External Libraries: numpy, matplotlib, scipy


License
MIT License


 Citation
Mehta, M. (2025). Comparative Analysis of A* and Dijkstra for Path Planning in Duckietown. B.Sc. Thesis, [Constructor University].
