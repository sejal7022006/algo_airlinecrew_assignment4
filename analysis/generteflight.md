# Problem 1 — Generate Flights  
## Summary & Complexity Analysis

### 📌 Objective  
The goal of this task is to create a function that generates a list of n random flights.  
Each flight is represented as a tuple:
The function randomly assigns:
- A start time (within a given range), and  
- A duration (1–4 hours, or as specified)

This flight dataset is used in later tasks for constraint checking and backtracking scheduling.

---

## 🧠 Algorithm Description  
For each flight:
1. Generate a random duration.  
2. Generate a random start time.  
3. Compute the end time = start + duration.  
4. Append the flight tuple to the list.

The function completes after generating all n flights.

---

## ⏱ Time Complexity Analysis  
The function performs *one loop of size n*, generating exactly one tuple per iteration.

### *Time Complexity*
\[
T(n) = O(n)
\]

### ✔ Experiment Results  
- Execution time increases steadily and linearly as n increases.  
- Graph confirms a straight, linear upward trend.  

This matches theoretical O(n) complexity.

---

## 💾 Space Complexity Analysis  
The output list stores n flight records, each a small tuple.

### *Space Complexity*
\[
S(n) = O(n)
\]

### ✔ Experimental Observation  
- Memory usage grows proportionally to the number of flights stored.  
- Graph shows clear linear behavior.

---

## ✅ Conclusion  
The flight generation function is efficient and scalable:

| Aspect | Complexity | Behavior |
|--------|------------|----------|
| Time   | *O(n)*   | Linear growth |
| Space  | *O(n)*   | Linear growth |

It is fast, lightweight, and suitable for preparing input data for constraint checking and backtracking in l
