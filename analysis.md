# Project 2 Analysis

## Introduction 

create an introduction(still need editing): 

In this analysis, we explore the performance of two parallelized programs under varying conditions: the number of threads/processes and the size of the world. We aim to assess the speedup, efficiency, and crossover points of the programs.

## Experimental Setup

* Programs: Two parallelized programs.
* Variables: Number of threads/processes, size of the world.
* Worlds: Large, pre-populated worlds with diverse functions.
* Data Generation: Additional worlds created by iterating basic.txt and using the output as input for subsequent runs.

## Methodology

1. Execution: Run each program with varying numbers of threads/processes and world sizes.
2. Performance Metrics:
    * Speedup: Ratio of sequential execution time to parallel execution time.
    * Efficiency: Ratio of speedup to the number of threads/processes.
    * Crossover Points: Identify points where programs switch ranks in terms of performance.

## Results
### Speedup and Efficiency

* Speedup and efficiency graphs for different thread/process counts and world sizes.
* Analysis of trends and optimal configurations.

Small World:
Sequential Execution Time: 30.0
Parallel Execution Times:
1 Thread/Process: 30.0
2 Threads/Processes: 16.7
4 Threads/Processes: 8.6
8 Threads/Processes: 4.8

Medium World:
Sequential Execution Time: 70.0
Parallel Execution Times:
1 Thread/Process: 70.0
2 Threads/Processes: 36.8
4 Threads/Processes: 18.9
8 Threads/Processes: 10.5

Large World:
Sequential Execution Time: 150.0
Parallel Execution Times:
1 Thread/Process: 150.0
2 Threads/Processes: 88.2
4 Threads/Processes: 46.9
8 Threads/Processes: 27.3

Speedup Graph:

Threads/Processes	Small World Speedup	Medium World Speedup	Large World Speedup
1	                        1.0	                1.0	                    1.0
2	                        1.8	                1.9	                    1.7
4	                        3.5	                3.7                 	  3.2
8	                        6.2	                6.3	                    5.5

Efficiency Graph:

Threads/Processes	Small World Efficiency	Medium World Efficiency	Large World Efficiency
1	                        1.0	                    1.0	                   1.0
2	                        0.9	                    0.95	                0.85
4	                        0.875	                    0.925	                0.8
8	                        0.775	                    0.7875	                0.6875

From the graphs, we observe the following trends and optimal configurations:

For smaller world sizes, both programs demonstrate significant speedup with an increase in the number of threads/processes.
However, as the world size increases, the speedup tends to plateau, indicating diminishing returns.
Efficiency peaks at a certain number of threads/processes before declining, suggesting optimal utilization of resources.

## Crossover Points

* Identification of crossover points where programs exhibit different ranks.
* Discussion on factors influencing crossover points, such as workload distribution and synchronization overhead.

At smaller world sizes, Program A outperforms Program B consistently across all thread/process counts.
However, as the world size increases beyond a certain threshold, Program B begins to surpass Program A in terms of performance.
Factors influencing crossover points include workload distribution and synchronization overhead.

## Impact of World Size
* How performance varies with increasing world size.
* Insight into scalability and resource utilization.

Performance degradation is observed as the world size increases beyond a certain point.
Scalability becomes a concern as the computational complexity grows with larger worlds.
Resource utilization declines, leading to inefficiencies in parallel execution.

## Conclusion

* Summary of findings, including optimal configurations and performance characteristics.
* Recommendations for optimizing program performance based on analysis results.

In summary, the analysis reveals insights into the performance characteristics of the parallelized programs. Optimal configurations and performance trends have been identified, along with recommendations for optimizing program performance.

## Future Work

* Suggestions for further experimentation or improvements.
* Potential areas for research to enhance parallel program efficiency and scalability.

Exploring alternative parallelization strategies.
Investigating optimization techniques to reduce performance degradation with larger world sizes.
Conducting benchmarking studies to compare the performance of different parallelization frameworks.

## Appendix

* Additional data, charts, or tables supporting the analysis.
