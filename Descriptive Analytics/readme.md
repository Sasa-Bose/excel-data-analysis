# 📘 Descriptive Analytics – Case Study 1 (CS1)

## 🏭 Overview

**Descriptive Analytics – Case Study 1** is an Excel-based analytics project that explores production data from a manufacturing department operating three CNC machining lines. The project applies statistical techniques—both descriptive and probabilistic—to evaluate production performance and estimate raw material needs.

---

## 📂 Case Study Context

- The department runs **3 CNC machining lines**, each consisting of **3 machines arranged in series**.
- Every part must pass through all machines on a line.
- Each machine introduces a **specific reject rate**, reducing the number of usable parts.
- Data covers **25 consecutive 8-hour shifts** per line, with output measured in pieces per shift.

---

## 🧱 Machine Line Structure & Reject Rates

Each CNC line consists of **3 machines in series**, with individual reject rates. These rejection rates are critical in determining how much raw material is needed to produce the final output.

![Machine Flow with Reject Rates](Machine lines with reject rates.png)

> **r** = reject rate per machine (in red).  
> Final effective yield per line = Product of yields from all 3 machines.  
> Example for Line A:  
> `Yield = (1 - 0.073) × (1 - 0.022) × (1 - 0.033) ≈ 89.78%`

---

## 🎯 Objectives

This case study aims to:

1. 📊 Describe the **expected production output range** of the department.  
2. 📦 Estimate **raw material requirements** considering cumulative reject rates.  
3. 📈 Use **probabilistic modeling (NORMINV)** to understand output variability.

---

## 📈 Analytical Features

### ✅ Non-Parametric Statistics

Calculated for each line's shift-wise production:

- Minimum & Maximum
- Range
- Median
- Quartiles (Q0 to Q4)
- Interquartile Range (IQR)

### ✅ Parametric Statistics

- Sample Mean & Standard Deviation
- **Expected Range using ±3σ (Empirical Rule)**

| Metric                  | Line A   | Line B   | Line C   |
|-------------------------|----------|----------|----------|
| Mean                    | 796.92   | 548.84   | 1002.52  |
| Std Deviation           | 9.71     | 5.01     | 30.43    |
| Max Expected (+3σ)      | ≈825.05  | ≈563.87  | ≈1093.81 |
| Min Expected (−3σ)      | ≈768.79  | ≈533.81  | ≈911.23  |
| Expected Range          | ≈56.26   | ≈30.06   | ≈182.58  |

### ✅ Probabilistic Analysis (NORMINV)

Estimated output levels based on selected probabilities:

| Probability Metric      | Line A   | Line B   | Line C   |
|-------------------------|----------|----------|----------|
| P(≤66.7%)               | 801.11   | 551.00   | 1015.66  |
| P(≤33.3%)               | 792.73   | 546.68   | 989.38   |
| **Middle third** range  | 8.38     | 4.33     | 26.27    |
| P(≤70%)                 | 802.01   | 551.47   | 1018.48  |

> 📌 Powered by Excel’s `NORMINV()` function.

### ✅ Raw Material Estimation

Calculates raw material input required to meet observed output:
Material Required = Final Output / (Yield₁ × Yield₂ × Yield₃)

Reject rates are compounded across each machine in the line.

---

## 🛠️ Tools Used

- **Microsoft Excel**
- Excel formulas: `AVERAGE`, `STDEV`, `QUARTILE`, `NORMINV`, etc.
- No VBA or macros used

---

## 📋 How to Use

1. Open the Excel workbook.
2. Review:
   - Data sheets: Shift-wise production for each CNC line.
   - Summary sheets: Statistical outputs and range estimations.
   - Material estimation tables.
   - Probability-based projections using `NORMINV()`.
3. Customize inputs (reject rates, probability values) to simulate scenarios.

---

## 🚧 Limitations

- Assumes reject rates are constant per machine and per shift.
- No modeling of downtime or rework.
- Assumes normal distribution for NORMINV-based projections.

---

## 📄 License

Released under the **MIT License**.

---

## 👤 Author

Created by [Sasa Bose]  
📧 Contact: [sasabose121@gmail.com]  
💬 Contributions, feedback, and forks are welcome!



