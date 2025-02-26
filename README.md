# Vehicle Routing Problem (VRP) for Last-Mile Delivery Optimization

### Overview

This project aims to solve the Multi-Depot Vehicle Routing Problem (MDVRP) by optimizing delivery routes from multiple depots to a set of customers. The main objectives are to minimize travel costs, improve delivery efficiency, and balance the workload among depots.

###  Objective

The main goal of this project is to:

1. **Optimize Delivery Routes**: Reduce the total travel distance for delivery vehicles while ensuring customer demands are met.
2. **Evaluate Heuristic Algorithms**: Assess the performance of algorithms like the Nearest Neighbor heuristic, 2-opt optimization, and a hybrid approach.
3. **Improve Upon Baseline Solutions**: Highlight improvements in route efficiency through heuristic optimizations.

### Dataset

The dataset used in this project is contained in the file 19MDVRP Problem Sets.xlsx. The dataset is sourced from an Excel file containing multiple MDVRP scenarios, each under a separate sheet named 'Problem 1', 'Problem 2', ..., up to 'Problem 19'.

- Currently, the code explicitly loads the sheet named 'Problem 1'.
- Future analysis can be extended to other problems by modifying the sheet name in the code.

It includes:

- **x coordinate**: X-axis location of customers.
- **y coordinate**: Y-axis location of customers.
- **Depot x coordinate**: X-axis location of the depot.
- **Depot y coordinate**: Y-axis location of the depot.
- **Customer Number**: Unique identifier for customers.
- **Demand**: The number of units each customer requires (if applicable).

### Heuristic Algorithms

#### Nearest Neighbor Heuristic

The **Nearest Neighbor** heuristic builds a route by iteratively visiting the nearest unvisited customer from the current location until all customers have been visited. While simple, this approach can provide a quick initial solution for route planning.

#### 2-opt Optimization

The **2-opt** optimization is a local search algorithm that attempts to improve an existing route by iteratively reversing segments of the route and checking whether this leads to a reduction in the total travel distance. The 2-opt method helps eliminate unnecessary detours, resulting in a shorter route.

### Performance Evaluation

- Nearest Neighbor Cost: 478.42
- Optimized Cost (2-Opt): 430.72
- Total Improvement: The 2-Opt algorithm improved the route by reducing the total cost by approximately 10%.

### Results

- The Nearest Neighbor Heuristic provided an initial route with a total cost of 478.42.
- After applying the 2-Opt Algorithm, the optimized route cost was reduced to 430.72, achieving a 9.97% reduction in total travel cost.

### Future Directions

1. Extend the analysis to other problems (2 to 19) for a comprehensive evaluation.
2. Explore advanced metaheuristics like Tabu Search or Genetic Algorithms.
3. Implement visualization tools to display optimized routes.

### Source

https://www.kaggle.com/datasets/adamjoseph7945/vehicle-routing-problem-set

