# Gurobi

The Gurobi Optimizer is a mathematical optimization software library for solving mixed-integer linear and quadratic optimization problems.
## Installation

Use this link [pip](https://www.gurobi.com/solutions/gurobi-optimizer/?campaignid=2027425882&adgroupid=138872525480&creative=596136109131&keyword=install%20gurobi%20python&matchtype=e&gclid=EAIaIQobChMI-ZLoq4nr-wIVxbLVCh3y5gIjEAAYASAAEgLpH_D_BwE) to install gurobi.

```bash
pip install gurobipy
```

## Usage

```python
from gurobipy import *
m = Model("PL-OBJ1")

# To add a variable
m.addVar()

# To add a constraint
m.addConstr()

# To add the objective function
# For exemple to maximize the objective_function
m.setObjective(objectif_function, GRB.MAXIMIZE)

# To update the model
m.update()

# Resolution
m.optimize()
```

## Project

The DARP that we deal with in our project is a transport on demand problem, in which
we work on two main objectives, maximizing the number of customers served and
minimization of the total travel time of all the requests served, while respecting a certain
number of constraints related to the capacity of each vehicle, the maximum duration of each request,
the windows of time and the salary of each driver. We proceed by a search in the
literature, a vision of a better understanding of the subject, then a formalization of the problem,
then we worked on two milestones: the first with the Gurobi optimizer to find a solution
accurate, valid and efficient with daily data (small data set), and the second with a
heuristic process in order to work on the weekly data and find a valid solution
and as optimal as possible.

