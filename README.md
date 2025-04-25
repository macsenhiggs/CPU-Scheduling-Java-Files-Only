# CPU Scheduling Algorithms Comparison

This project is a comparative analysis of six CPU scheduling algorithms implemented in Java, designed to evaluate their performance under a variety of simulated conditions. Developed as part of an undergraduate Operating Systems course (CS 3502), the project investigates the strengths and weaknesses of both classic and modern scheduling methods through data-driven testing and visualization.

## 📋 Algorithms Implemented

- **First Come First Serve (FCFS)**
- **Shortest Job First (SJF)**
- **Round Robin**
- **Priority Scheduling**
- **Shortest Time Remaining First (STRF)** – ✨ *new*
- **Highest Response Ratio First (HRRF)** – ✨ *new*

## 🛠️ Project Structure

- `Process.java` – Defines custom process objects with key scheduling attributes (AT, BT, WT, TAT, etc.)
- `Scheduler.java` – Contains logic for each of the six scheduling algorithms
- `CSVWriter.java` – Utility class for outputting test results to CSV files
- `Execute.java` – Main driver that runs simulations and aggregates results
- `/results/` – Folder containing CSV output from each test
- `/figures/` – Box plots generated via R (using `ggplot2`)

## 📊 Testing Strategy

Five unique test cases were developed to simulate various CPU loads and process configurations:

1. **`smallTest`** – Simple 3–5 process test for manual validation
2. **`largeTest`** – General-purpose load with 10–50 processes
3. **`sameBTandAT`** – All processes arrive at once with similar bursts
4. **`longAndShort`** – Mix of short and long processes to evaluate balance
5. **`shrinking`** – Descending burst sizes to highlight preemption behavior

Each scheduling method was run **100 times per test**, and the results were analyzed using box plots in R to evaluate:

- Average Turnaround Time (TAT)
- Average Wait Time (WT)
- CPU Utilization (%)
- Throughput

> TAT was identified as the most valuable metric for performance comparison.

## 🧠 Key Findings

- **STRF and HRRF** consistently outperformed all other methods in terms of turnaround time.
- **Round Robin** was the least efficient overall but useful for avoiding starvation.
- **SJF** proved to be the best of the original four and performed closely to STRF and HRRF in most tests.
- **Preemptive algorithms** generally yielded better outcomes in scenarios with diverse burst times.

## 🧪 Visualization

All test data was exported as CSV and plotted using the `ggplot2` library in R. See `/figures/` for full result visualizations.

![TAT Comparison Example](figures/largeTestResults.png)

## 🧰 Technologies Used

- Java (OpenJDK 21)
- LaTeX (Report preparation)
- R + ggplot2 (Data visualization)
- CSV for structured data output

## 📚 References

- [FrancisNweke/CPU-Simulator-GUI](https://github.com/FrancisNweke/CPU-Simulator-GUI)
- [Wikipedia - Highest Response Ratio Next](https://en.wikipedia.org/wiki/Highest_response_ratio_next)
- [The R Graph Gallery - Boxplot](https://r-graph-gallery.com/boxplot.html)

## 👨‍💻 Author

**Macsen Higgins**  
Kennesaw State University  
CS 3502 - Section 03  
April 2025  
mhiggi36@students.kennesaw.edu

---

