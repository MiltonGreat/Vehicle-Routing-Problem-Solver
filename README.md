# Vehicle Routing Problem (VRP) for Last-Mile Delivery Optimization

### Overview

**In modern logistics, an optimized route is not just the shortest path—it's the most resilient, equitable, and sustainable one.** This project conducts a governance audit of a Vehicle Routing Problem (VRP) solver for last-mile delivery. We move beyond minimizing distance to critically evaluate the routing system's robustness to disruption, its inherent fairness to different communities, and its alignment with broader corporate ESG goals. While the 2-opt algorithm achieved a 10% reduction in travel cost, the true value lies in building a routing system that serves as a reliable component of your Digital Supply Chain Control Tower.

###  Supply Chain Problem: The Hidden Costs of "Optimal" Routes

Traditional route optimization focuses solely on cost and distance, creating systems that are efficient yet fragile. An ungoverned routing algorithm introduces critical risks:

- Resilience Risk: A route that is optimal in perfect conditions may fail completely if a key road is closed or a depot goes offline.

- Equity Risk: A system that minimizes total distance might systematically avoid low-density or remote areas, creating "delivery deserts" and disadvantaging certain customer demographics.

- ESG Risk: The shortest route is not always the most sustainable. It might direct heavy traffic through residential neighborhoods or fail to prioritize low-emission delivery windows.

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

### Our Approach: The Routing System Resilience Audit

We applied a multi-dimensional governance framework to stress-test the routing algorithm beyond simple cost metrics.

1. **The Pre-Launch “Resilience Stress Test”**

Scenario Modeling: We evaluated the algorithm's performance under disruption. How does the route degrade if Depot A becomes inoperable? Can the system dynamically re-allocate vehicles and customers to other depots without catastrophic failure? A resilient system must gracefully degrade, not catastrophically fail.

Workload Balance Audit: We analyzed the solution for operational fairness across depots and drivers. An "optimal" solution that overloads one depot while under-utilizing others creates a single point of failure and leads to driver burnout.

2. **The Fairness and Impact Audit**

Service Equity Check: We audited the routing output for geographic bias. Does the model consistently service high-density, high-value urban centers at the expense of suburban or rural customers? This isn't just an ethical question—it's a missed market opportunity and a potential reputational risk.

Community Impact Assessment: The model's objective was to minimize distance. However, a governance framework would force us to ask: Does this route concentrate truck traffic and emissions through sensitive areas like school zones or low-income neighborhoods?

### Heuristic Algorithms

#### Nearest Neighbor Heuristic

The **Nearest Neighbor** heuristic builds a route by iteratively visiting the nearest unvisited customer from the current location until all customers have been visited. While simple, this approach can provide a quick initial solution for route planning.

#### 2-opt Optimization

The **2-opt** optimization is a local search algorithm that attempts to improve an existing route by iteratively reversing segments of the route and checking whether this leads to a reduction in the total travel distance. The 2-opt method helps eliminate unnecessary detours, resulting in a shorter route.

### Audit Results & Strategic Interpretation

- Cost Efficiency	- 9.97% reduction (478.42 to 430.72) PASS. The algorithm successfully optimizes for its primary financial objective.
- Algorithmic Resilience - Not explicitly tested for depot failure. HIGH RISK. The model's performance under disruption is unknown. It may be highly fragile.
- Operational Fairness - Workload balance not a primary constraint. MODERATE RISK. Could lead to imbalanced resource use and driver dissatisfaction.
- ESG Alignment	- No emissions or community impact factored. FAIL. The model optimizes for a narrow financial goal, potentially creating negative externalities.

### Conclusion

The 10% cost reduction is a tactical win, but it represents a fragile efficiency. Deploying this system at scale without governance controls would create a logistics network that is highly optimized for yesterday's conditions and wholly unprepared for tomorrow's disruptions.

### Source

https://www.kaggle.com/datasets/adamjoseph7945/vehicle-routing-problem-set

