# Dynamic Programming and Optimal Control
The goal of this programming exercise was to was to deliver a package with a drone as quickly as possible when the system dynamics are subject to probabilistic uncertainty.
## Problem set up
<img align="right" height="140" src="https://github.com/andreadacol98/Dynamic_Programming/blob/main/Images/UAV.PNG"></img>
The drone operates in a discretized world of M x N cells and its dynamics at a certain time step are modelled through three state variables, namely its position on the <i>x</i> and <i>y</i>-axis and a binary variable telling if the UAV is carrying the package or not. 
At time step <i>k</i> the system evolves in the following way:
<ul>
  <li>One of the allowable control inputs <i>u<sub>k</sub></i> is applied. In particular <i>u<sub>k</sub></i> &isin; {North, South, East, West, Hover}. However the control input is not allowed if it leads ouside the world boundaries or against and obstacle;</li>
  <img align="right" height="140" src="https://github.com/andreadacol98/Dynamic_Programming/blob/main/Images/grid_world.png"></img>
  <li>From the new desired position, a gust of wind, occurring with probability <i>p<sub>wind</sub></i>, moves the drone either North, South, East and West uniformly at random;</li>
  <li>The drone crashes if it ends up outside the grid world boundaries or against the obstacles;</li>
  <li>Whenever a drone crashes it is brought to a base station carrying no package. The fixing procedure takes <i>N<sub>c</sub></i> time steps.</li>
</ul>

## Tasks
Find the policy minimizing the expected number of time steps needed to deliver a package by using the following methods for the Infinite Horizon problem:
<ul>
  <li>Value Iteration;</li>
  <li>Policy Iteration;</li>
  <li>Linear Programming.</li>
</ul>

Further Info in "Assignment.pdf"





