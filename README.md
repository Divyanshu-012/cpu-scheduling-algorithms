# CPU-Scheduling-Algorithms
This project implements several CPU scheduling algorithms in C++ to simulate and analyze how different scheduling strategies affect process execution in an operating system. The algorithms included are:

First Come First Serve (FCFS)

Round Robin (RR) with variable time quantum

Shortest Process Next (SPN)

Shortest Remaining Time (SRT)

Highest Response Ratio Next (HRRN)

Feedback (FB) and Feedback with variable time quantum (FBV)

Aging
## Table of Contents
Algorithms

Installation

Input Format

Contributing

## Algorithms

1. First Come First Serve (FCFS)

FCFS executes processes in the order they arrive.

Non-preemptive: once a process starts, it runs until completion.

Simple to implement but can cause long processes to block shorter ones.

2. Round Robin (RR)

RR assigns each process a time slice (quantum) to execute.

If a process is not finished within its quantum, it goes back to the end of the queue.

Time quantum can be adjusted dynamically for better efficiency.

3. Shortest Process Next (SPN)

SPN executes the process with the shortest burst time first.

Non-preemptive, prioritizes reducing the average waiting time.

4. Shortest Remaining Time (SRT)

Preemptive version of SPN.

Processes with shorter remaining time can interrupt currently running processes.

5. Highest Response Ratio Next (HRRN)

Non-preemptive algorithm that selects the process with the highest response ratio:

Response Ratio
=
Waiting Time
+
Burst Time
Burst Time
Response Ratio=
Burst Time
Waiting Time+Burst Time
	​


Helps prevent starvation of long processes.

6. Feedback (FB)

Multi-level priority scheduling.

Processes can move to lower-priority queues after completing a time slice.

7. Feedback with variable quantum (FBV)

Similar to FB but assigns different quanta based on queue levels.

Optimizes CPU allocation for high-priority processes.

8. Aging

Prevents starvation by gradually increasing the priority of waiting processes.

Ensures that even low-priority processes eventually get CPU time.



## Installation
1- Clone the repository

git clone https://github.com/Divyanshu-012/CPU-Scheduling-Algorithms.git
cd CPU-Scheduling-Algorithms

2- Install the C++ compiler and make:

sudo apt-get install g++ make


3- Compile the project using make:

make

4- Run the executable:

./cpu_scheduling

## Input Format
1. First line: "trace" or "stats"

2. Second line: comma-separated list of scheduling policies and their parameters (e.g., 2-4 for RR with quantum 4).

3. Third line: last instant of the simulation timeline.

4. Fourth line: number of processes.

5. Process details (one per line):

- For algorithms 1–7: ProcessName, ArrivalTime, ServiceTime

- For Aging (algorithm 8): ProcessName, ArrivalTime, Priority

Processes must be sorted by arrival time. If two processes have the same arrival time, the one with lower priority comes first.

## Contributing

Contributions, suggestions, and feedback are welcome. Feel free to open issues or submit pull requests to improve the project.
