# CPU Scheduling Algorithms Comparison

This project is a comparative analysis of six CPU scheduling algorithms implemented in Java, designed to evaluate their performance under a variety of simulated conditions. Developed as part of an undergraduate Operating Systems course (CS 3502), the project investigates the strengths and weaknesses of both classic and modern scheduling methods through data-driven testing and visualization.

## 📋 Algorithms Implemented

- **First Come First Serve (FCFS)**
- **Shortest Job First (SJF)**
- **Round Robin**
- **Priority Scheduling**
- **Shortest Time Remaining First (STRF)** *new*
- **Highest Response Ratio First (HRRF)** *new*

## 🛠️ Project Structure

- `Process.java` – Defines custom process objects with key scheduling attributes (AT, BT, WT, TAT, etc.)
- `Scheduler.java` – Contains logic for each of the six scheduling algorithms
- `CSVWriter.java` – Utility class for outputting test results to CSV files
- `Execute.java` – Main driver that runs simulations and aggregates results

## 📊 Testing Strategy

Five unique test cases were developed to simulate various CPU loads and process configurations:

1. **`smallTest`** – Simple 3–5 process test for manual validation
2. **`largeTest`** – General-purpose load with 10–50 processes
3. **`sameBTandAT`** – All processes arrive at once with similar bursts
4. **`longAndShort`** – Mix of short and long processes to evaluate balance
5. **`shrinking`** – Descending burst sizes to highlight preemption behavior

Each scheduling method was run **100 times per test**, and the results can be analyzed using box plots in R to evaluate:

- Average Turnaround Time (TAT)
- Average Wait Time (WT)
- CPU Utilization (%)
- Throughput

---

