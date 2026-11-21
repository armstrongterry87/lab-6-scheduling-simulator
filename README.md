# Lab 6: Scheduling Simulator

A C simulation of four CPU scheduling algorithms. For each one it prints every
process's burst, waiting and turnaround time, plus the averages.

1. First Come First Serve (FCFS)
2. Shortest Job First, preemptive (SJF / SRTF)
3. Priority (higher `pri` value runs first, then FCFS)
4. Round Robin (quantum = 2)

## Build and run

```
gcc -Wall -std=gnu99 -Werror -pedantic -g schedsim.c util.c -o schedsim
./schedsim input0.txt
```

Each input line is: `pid burst_time arrival_time wait_time turnaround_time priority`.

## Files

- `schedsim.c`: the scheduling algorithms and driver
- `util.c`, `util.h`: input file parsing
- `process.h`: the `ProcessType` struct
- `input0.txt`, `input1.txt`, `input2.txt`: sample inputs
