# Benchmark Dataset for Flexible Job Shop Scheduling Problem (FJSP)

This dataset contains 60 benchmark instances (D01-D60) for the Flexible Job Shop Scheduling Problem (FJSP). Each instance consists of three parts, describing the problem size, operation configurations, and setup time configurations. The dataset is designed to facilitate research and development of scheduling algorithms.

---

## **Dataset Structure**

Each instance is divided into three parts:

### **1. Problem Size**
The first line contains 7 numbers, representing the following:
1. **Number of jobs**: Total number of jobs.
2. **Maximum number of operations per job**: Maximum number of operations that any job can have.
3. **Number of machines**: Total number of machines available.
4. **Maximum number of tools per tool type**: Maximum number of tools that belong to each tool type.
5. **Number of tool types**: Total number of tool types.
6. **Expectation of processing time**: Average processing time for operations.
7. **Expectation of tool-switching setup time**: Average setup time required for tool switching.

**Example**:
```
10 5 6 5 5 50 5
```
- 10 jobs,
- Each job has up to 5 operations,
- 6 machines,
- Up to 5 tools per tool type,
- 5 tool types,
- Average processing time of 50,
- Average tool-switching setup time of 5.

---

### **2. Operation Configurations**
This section describes the configuration of each operation. The number of rows equals the total number of operations across all jobs. Each row contains the following information:
1. **Index of jobs**: Job ID.
2. **Index of operations**: Operation ID within the job.
3. **Available machine number**: Number of machines available for this operation.
4. **Machine indices**: List of machine IDs available for this operation.
5. **Processing time of operation**: List of processing times corresponding to each machine.
6. **Tool type**: Tool type required for this operation.
7. **Available tool number**: Number of tools available for this tool type.
8. **Tool indices**: List of tool IDs available for this tool type.

**Example**:
```
1 1 6 [1 2 3 4 5 6] [36 53 59 45 56 59] 4 5 [20 21 22 23 24]
```
- Job 1, Operation 1,
- 6 available machines (IDs: 1, 2, 3, 4, 5, 6),
- Processing times: 36, 53, 59, 45, 56, 59 (corresponding to each machine),
- Tool type: 4,
- 5 available tools (IDs: 20, 21, 22, 23, 24).

---

### **3. Setup Time Configurations**
This section defines the setup time required for tool switching on each machine. Each row contains the following information:
1. **Index of machine**: Machine ID.
2. **Previous index of tool**: Tool ID before switching.
3. **Current index of tool**: Tool ID after switching.
4. **Setup time**: Time required for the tool switch.

**Example**:
```
1 20 21 5
```
- Machine 1,
- Switching from tool 20 to tool 21,
- Setup time: 5.

---

## **Dataset Usage**
This dataset is suitable for:
- Developing and testing scheduling algorithms (e.g., heuristic, metaheuristic, or exact methods).
- Benchmarking performance for Flexible Job Shop Scheduling Problems (FJSP).
- Studying the impact of tool switching and setup times on scheduling.

---

## **File Naming Convention**
The dataset consists of 60 instances, named `D01` to `D60`. Each file contains the three parts described above.

---

## **License**
This dataset is provided for academic and research purposes. Please cite the original source if you use this dataset in your work.

---

## **Contact**
For questions or feedback, please contact admin@walkcap.com.

---
