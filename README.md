# CI2024_lab2
<br>

## Trivial approach
- **Best greedy solution** (*approach 1*): it maximizes the optimization given by a single greedy solution (obtained at each step by adding the closest city). This approach requires an high execution time with large number of cities when using the geodesic function to represent distance.
## Hill climbers
- **Best greedy solution with 2-opt** (*approach 2*): it tries to further optimize the best greedy solution obtained in the previous algorithm by applying a simple 2-opt tweak. Unfortunately this approach seems unable to improve the greedy solution (the only improvements are sometimes in the order of 3-4 kilometers, so almost negligible).
- **Hill climbing with 2-opt and simulated annealing** (*approach 3*): it uses 2-opt (repeated multiple times according to a temperature value) in order to optimize a random starting solution. In this case the result has a huge improvement (for example about 6000 kilometers for Russia), but this is not enough to produce a better result than the greedy one given that the starting solution has often a very bad fitness.
- **Best greedy solution with insert mutation** (*approach 4*): it repeats the process of the approach 2 but using a different mutation function. Insert mutation does not seem to produce different results with respect to 2-opt with greedy solution.
- **Hill climbing with insert mutation and simulated annealing** (*approach 5*): it repeats the process of the approach 3 but using insert mutation. Again, the final solution is not improved enough to be better than the greedy one, while the execution time is greatly reduced.
## Evolutionary algorithm
- **EA approach** (*approach 6*): this approach uses an evolutionary algorithm based on tournament selection, inver over crossover and insert mutation. This algorithm, in spite of requiring longer execution time, it produces better results than the previous hill climber approaches. 
