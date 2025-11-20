### 📌 Objective  
Create a *Gantt chart* to visually represent the flight schedule assigned to each crew member.

A Gantt chart shows:
- Crew members on the Y-axis  
- Flight time slots on the X-axis  
- Bars representing individual flights  
- Labels identifying each flight  

This provides a clear visual verification of the schedule.

---

## 🧠 How the Gantt Chart Works  
For each crew member:
1. Get all flights assigned to them.
2. Plot each flight as a horizontal bar:
   - Length = end_time – start_time
   - Position = start_time  
3. Add flight label (e.g., F1, F2)

---

## ⏱ Time Complexity Analysis  
The chart draws one bar per flight.

If there are n flights:

\[
T(n) = O(n)
\]

### Observation  
- Plotting time grows linearly with the number of bars.

---

## 💾 Space Complexity Analysis  
Space required is proportional to the number of rectangles drawn:

\[
S(n) = O(n)
\]

The chart renders visually but does not consume exponential memory.

---

## 🎨 Conclusion  
Gantt charts are an effective visual tool:

- They validate flight sequences  
- Show overlaps immediately  
- Help compare crew workloads  

They run in *O(n)* time and space, making them efficient for the visualization part of the scheduling problem.

---
