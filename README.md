# Implementation of Tabu Search optimization to solve the Quadratic Assignment Problem (QAP)
This code is an implementation of Tabu Search to solve the Quadratic Assignment Problem (QAP) test problems 
of Nugent et al (20 department). The objective is to minimize flow costs between the placed departments. The 
flow cost is (flow * distance), where both flow and distance are symmetric between any given pair of departments. 

For the simple Tabu search implementation, I applied the swap as a move operator. Accordingly, to move from the 
current solution, neighbors of n combination 2 are created and sorted based on their cost value. The solutions 
accepted over the course of the search are added to the tabu list to forbid going back to the already visited 
solutions. When the tabu list size is exceeded, the old solutions in the list are deleted. Since I am using double 
cost, I am expecting an optimal value of 2570. From the repeated experiments, I realized that tabu size of 17 works 
better than other values. I did several experiments, and recorded only some of them which provides clear implication 
of changes in the experimental results as described in the assignment problem. 

The optimal solution is [17,13,9,2,8,3,1,11,10,15,18,14,19,7,12,16,4,6,0,5], which is equal to 
[18,14,10,3,9,4,2,12,11,16,19,15,20,8,13,17,5,7,1,6] if the location counter index starts from 0.


This implementaion consists of two variations of Tabu Search algorithm:
The recency based (short term memory) and frequency based (long term memory)