# Problem 3 — Backtracking Crew Assignment  
## Summary & Complexity Analysis

### 📌 Objective  
Assign each flight to one of the available crew members using a *backtracking search algorithm*, ensuring:

- No overlapping flights  
- Required rest time  
- All flights must be assigned  

This forms the core scheduling mechanism for the airline crew problem.

---

## 🧠 Algorithm Description  
1. Sort flights by starting time.
2. For each flight:
   - Try assigning it to each crew member.
   - Use constraint checker from Problem 2.
   - If valid → continue recursively.
   - If invalid → backtrack.

3. Continue until:
   - A valid complete schedule is found, or  
   - All possibilities are exhausted.

---

## ⏱ Time Complexity Analysis  
Backtracking must explore multiple branches of possible assignments.

Worst-case:

\[
T(n) = O(k \cdot 2^n)
\]

k = number of crew  
n = number of flights

### ✔ Experimental Findings  
- Runtime grows slowly for n ≤ 6.  
- After n ≥ 7, runtime grows *exponentially*.  
- Graph shows rapid upward curve → confirming exponential growth.

---

## 💾 Space Complexity Analysis  
Space is used for:
- Flight list → O(n)  
- Recursion depth → O(n)  
- Crew assignment lists → O(n)

Total:

\[
S(n) = O(n)
\]

### ✔ Observed  
- Memory usage grows linearly with n.

---

## 🔁 Recursive Calls  
Recursive calls behave exponentially:

\[
\text{Calls} \approx O(2^n)
\]

Graph reflects steep exponential rise.

---

## ✅ Conclusion  
Backtracking guarantees correct scheduling but is not scalable for large n due to exponential time.  
It is excellent for small instances and for demonstrating CSP principles.

---
