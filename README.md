# Vehicle Routing Problem (VRP) for Last-Mile Delivery Optimization

### Overview

This project addresses the Vehicle Routing Problem (VRP), focusing on optimizing last-mile delivery routes for vehicles serving a set of customers from one or more depots. The primary objective is to minimize the total distance traveled by delivery vehicles while ensuring all customers are served efficiently. To achieve this, heuristic algorithms such as Nearest Neighbor and 2-opt local search were implemented and evaluated. The project leverages customer and depot location data to generate and improve delivery routes.

###  Objective

The main goal of this project is to:

1. **Optimize Delivery Routes**: Reduce the total travel distance for delivery vehicles while ensuring customer demands are met.
2. **Evaluate Heuristic Algorithms**: Assess the performance of algorithms like the Nearest Neighbor heuristic, 2-opt optimization, and a hybrid approach.
3. **Improve Upon Baseline Solutions**: Highlight improvements in route efficiency through heuristic optimizations.

### Problem Statement

Efficient route planning is a critical challenge in logistics, with implications for reducing delivery costs, improving customer satisfaction, and minimizing environmental impact. This project aims to:

- Develop algorithms that minimize travel distance and time.
- Provide scalable solutions that adapt to various logistical scenarios.
- Ensure solutions are computationally efficient and practical for real-world deployment.

### Dataset

The dataset used in this project is contained in the file 19MDVRP Problem Sets.xlsx. It consists of customer and depot locations, represented as x and y coordinates, and includes additional information relevant to the VRP. It includes:

- **x coordinate**: X-axis location of customers.
- **y coordinate**: Y-axis location of customers.
- **Depot x coordinate**: X-axis location of the depot.
- **Depot y coordinate**: Y-axis location of the depot.
- **Customer Number**: Unique identifier for customers.
- **Demand**: The number of units each customer requires (if applicable).

### Solution Approach

Data: Traffic patterns, delivery windows, customer locations, and depot coordinates.

Methods:

- Modeled the Vehicle Routing Problem (VRP) with time constraints.
- Implemented heuristic optimization algorithms, such as Nearest Neighbor and 2-opt local search, to identify and improve routes.
- Evaluated route efficiency by comparing the initial and optimized delivery routes in terms of total distance and time.
- Tools: Python (NumPy, NetworkX, Matplotlib).

### Visualizations

The following visualizations are generated:

1. **Scatter Plots** of customer and depot locations to visually represent delivery points.
2. **Route Path**: The delivery route is plotted on a 2D plane showing the order in which customers are visited.
3. **Map Visualization**: Using `folium`, routes are plotted on a map to provide geographical context.

### Heuristic Algorithms

#### Nearest Neighbor Heuristic

The **Nearest Neighbor** heuristic builds a route by iteratively visiting the nearest unvisited customer from the current location until all customers have been visited. While simple, this approach can provide a quick initial solution for route planning.

#### 2-opt Optimization

The **2-opt** optimization is a local search algorithm that attempts to improve an existing route by iteratively reversing segments of the route and checking whether this leads to a reduction in the total travel distance. The 2-opt method helps eliminate unnecessary detours, resulting in a shorter route.

### Performance Evaluation

- Nearest Neighbor Cost: 478.42
- Optimized Cost (2-Opt): 430.72
- Total Improvement: The 2-Opt algorithm improved the route by reducing the total cost by approximately 10%.

### Key Insights

1. Optimization Impact:
- The 2-opt algorithm significantly improved route efficiency over the Nearest Neighbor baseline.

2. Practical Feasibility:
- Heuristic algorithms provide quick and effective solutions for real-world logistics problems.

### Future Directions

1. Dynamic Route Optimization:
- Integrate real-time traffic and weather data for adaptive routing.

2. Environmental Considerations:
- Include carbon footprint minimization as an optimization objective.

3. Advanced Algorithms:
- Explore machine learning approaches, such as reinforcement learning, for dynamic decision-making.

4. Multi-Objective Optimization:
- Simultaneously optimize for cost, time, and environmental impact.

### Source

https://www.kaggle.com/datasets/adamjoseph7945/vehicle-routing-problem-set

