# Assignment - Multi-Threading Performance Analysis

## Objective
To analyze the performance of matrix multiplication using multi-threading by varying the number of threads and observing execution time and CPU utilization.

---

## Problem Statement
Multiply multiple random matrices of size 2000 × 2000 with a constant matrix of the same size and analyze performance using different thread counts.

---

## System Configuration

- CPU Cores: 2  
- Threads Tested: 1 to 4 (2 × cores)  
- Matrix Size: 2000 × 2000  
- Number of Matrices: 300  

---

## Technologies Used

- Python  
- NumPy  
- Multiprocessing  
- Matplotlib  
- Psutil  

---

## Results

| Threads | Time (min) | Time (sec) |
|--------|-----------|-----------|
| T=1 | 1.8804 | 112.8 |
| T=2 | 1.8144 | 108.9 |
| T=3 | 1.7768 | 106.6 |
| T=4 | 1.7456 | 104.7 |

---

## Observations

- Execution time decreases slightly as the number of threads increases.
- Maximum performance achieved at T=4 threads.
- Improvement is not significant due to limited number of CPU cores.

---

## Analysis

- CPU usage is nearly 100% on both cores for all thread counts.
- Since the system has only 2 cores:
  - Additional threads (T > 2) do not provide significant speedup.
  - Threads compete for CPU resources.
- Minimal performance gain is observed due to:
  - Context switching overhead
  - Limited parallel hardware

---

## Conclusion

The performance improves slightly with increased threads, but due to only 2 CPU cores, the speedup is limited.

Optimal performance is achieved at higher thread counts, but the gain is marginal.

---

## Key Metrics

- Fastest Run: T=4 → 1.7456 min  
- Slowest Run: T=1 → 1.8804 min  
- Speedup (T1 → T4): **1.08×**

