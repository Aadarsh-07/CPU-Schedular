# CPU Scheduling Simulation

## Description
This project is a C++ implementation of three popular CPU scheduling algorithms:

1. **First-Come, First-Served (FCFS)**
2. **Shortest Job First (SJF)**
3. **Round Robin (RR)**

The program takes user input for process details (burst time and arrival time) and simulates the selected scheduling algorithm. It calculates and displays important metrics such as:

- Waiting Time (WT)
- Turnaround Time (TAT)

This project helps in understanding the working and comparison of different CPU scheduling techniques.

## Features
- **Interactive Interface**: Users can input process details and select the desired scheduling algorithm.
- **Modular Design**: Each scheduling algorithm is implemented as a separate function.
- **Flexible Round Robin**: Supports user-defined time quantum.
- **Detailed Output**: Displays process details including waiting and turnaround times.

## How It Works
1. The user provides the number of processes and their respective burst times and arrival times.
2. The user selects one of the three scheduling algorithms.
3. The program calculates waiting times and turnaround times based on the selected algorithm.
4. The results are displayed in a tabular format.

## Algorithms Implemented
### 1. First-Come, First-Served (FCFS)
Processes are executed in the order they arrive. It is a non-preemptive scheduling algorithm.

### 2. Shortest Job First (SJF)
Processes are selected based on their burst time, with shorter jobs executed first. This implementation assumes non-preemptive scheduling.

### 3. Round Robin (RR)
Processes are executed in a cyclic order with a fixed time quantum. This is a preemptive scheduling algorithm.

## Code Structure
- `struct Process`: Stores process details such as process ID, burst time, arrival time, waiting time, and turnaround time.
- `fcfs()`: Implements the First-Come, First-Served scheduling algorithm.
- `sjf()`: Implements the Shortest Job First scheduling algorithm.
- `roundRobin()`: Implements the Round Robin scheduling algorithm with user-defined time quantum.
- `printProcessDetails()`: Prints the details of all processes after scheduling.

## Example Output
### Input:
```
Enter the number of processes: 3
Enter burst time and arrival time for process 1: 5 0
Enter burst time and arrival time for process 2: 3 1
Enter burst time and arrival time for process 3: 8 2

Choose a scheduling algorithm:
1. First-Come, First-Served (FCFS)
2. Shortest Job First (SJF)
3. Round Robin (RR)
2
```

### Output:
```
PID	Burst	Arrival	Waiting	Turnaround
1	5	0	0	5
2	3	1	4	7
3	8	2	7	15
```

## How to Run
1. Clone this repository.
2. Compile the code using any C++ compiler, e.g.,
   ```
   g++ -o cpu_scheduling cpu_scheduling.cpp
   ```
3. Run the executable:
   ```
   ./cpu_scheduling
   ```
4. Follow the prompts to input process details and select an algorithm.

## Requirements
- C++ compiler (e.g., GCC, Clang, or MSVC)
- Basic understanding of CPU scheduling algorithms

## Contributions
Contributions are welcome! Feel free to submit issues or pull requests to improve the project.

