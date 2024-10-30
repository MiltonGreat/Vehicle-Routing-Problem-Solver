# Vehicle Routing Problem (VRP) for Last-Mile Delivery Optimization

## Project Overview

This project aims to solve the Vehicle Routing Problem (VRP), which focuses on optimizing last-mile delivery routes for vehicles serving a set of customers from one or more depots. The goal is to minimize the total distance traveled by delivery vehicles while ensuring all customers are served. In this project, we implemented heuristic algorithms such as Nearest Neighbor and 2-opt local search to generate and improve delivery routes. The algorithms are applied to a dataset containing customer locations and depot coordinates.

## Objective

The main goal of this project is to:

1. **Optimize Delivery Routes**: Minimize the total distance traveled by the vehicles while fulfilling all customer demands.
2. **Evaluate Heuristic Algorithms**: Implement and evaluate heuristic methods like the Nearest Neighbor heuristic, 2-opt optimization, and a hybrid approach.
3. **Improve Upon Baseline Solutions**: Compare the performance of the implemented algorithms to baseline solutions to measure improvement.

## Dataset
The dataset used in this project is contained in the file 19MDVRP Problem Sets.xlsx. It consists of customer and depot locations, represented as x and y coordinates, and includes additional information relevant to the VRP. It includes:

- **x coordinate**: X-axis location of customers.
- **y coordinate**: Y-axis location of customers.
- **Depot x coordinate**: X-axis location of the depot.
- **Depot y coordinate**: Y-axis location of the depot.
- **Customer Number**: Unique identifier for customers.
- **Demand**: The number of units each customer requires (if applicable).

## Heuristic Algorithms

### Nearest Neighbor Heuristic

The **Nearest Neighbor** heuristic builds a route by iteratively visiting the nearest unvisited customer from the current location until all customers have been visited. While simple, this approach can provide a quick initial solution for route planning.

### 2-opt Optimization

The **2-opt** optimization is a local search algorithm that attempts to improve an existing route by iteratively reversing segments of the route and checking whether this leads to a reduction in the total travel distance. The 2-opt method helps eliminate unnecessary detours, resulting in a shorter route.

### Performance Evaluation

- Nearest Neighbor Cost: 478.42
- Optimized Cost (2-Opt): 430.72
- Total Improvement: The 2-Opt algorithm improved the route by reducing the total cost by approximately 10%.

## Visualizations

The following visualizations are generated:

1. **Scatter Plots** of customer and depot locations to visually represent delivery points.
2. **Route Path**: The delivery route is plotted on a 2D plane showing the order in which customers are visited.
3. **Map Visualization**: Using `folium`, routes are plotted on a map to provide geographical context.

### Code Explanation and Key Insights

- The Nearest Neighbor algorithm generates an initial delivery route with a total cost of 478.42.
- The 2-Opt optimization reduces the cost to 430.72, achieving a 10% improvement.

### Source

https://www.kaggle.com/datasets/adamjoseph7945/vehicle-routing-problem-set

