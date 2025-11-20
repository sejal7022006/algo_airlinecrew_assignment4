# Problem 2 — Constraint Checking  
## Summary & Complexity Analysis

### 📌 Objective  
The purpose of this task is to verify whether a specific flight can be safely assigned to a crew member without violating scheduling constraints.

The two constraints checked are:
1. *No overlapping flights*  
2. *Minimum rest time* between consecutive flights for the same crew

These checks allow the backtracking algorithm (Problem 3) to prune invalid partial schedules early.

---

## 🧠 How the Constraint Checking Works  
For each new flight:
1. Compare it with every flight already assigned to the crew.
2. Check for time overlap:
   \[
   e1 + rest \le s2 \quad \text{OR} \quad e2 + rest \le s1
   \]
3. If overlap or rest violation occurs → assignment is *not allowed*.

---

## ⏱ Time Complexity Analysis  
Each new flight is compared with all flights in the crew’s schedule.

If the schedule has n flights:

\[
T(n) = O(n)
\]

### ✔ Experiment Results  
- Execution time increases linearly with n.  
- The plotted graph clearly supports O(n) complexity.

---

## 💾 Space Complexity Analysis  
Space is used only to store the schedule list and temporary variables.

\[
S(n) = O(n)
\]

### ✔ Observed  
- Memory increases linearly because the schedule stores n flights.  

---

## ✅ Conclusion  
Constraint checking is efficient with *linear time and space complexity*.  
It is a crucial pruning mechanism for backtracking and significantly reduces invalid search paths.

---
