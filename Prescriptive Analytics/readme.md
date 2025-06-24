# 📦 Prescriptive Analytics in Excel: Inventory Optimization with EOQ, EPQ, and Solver

This Excel project applies **prescriptive analytics** to help businesses determine optimal inventory ordering decisions. It uses **Economic Order Quantity (EOQ)**, **Economic Production Quantity (EPQ)**, and **Excel Solver** to compare and minimize inventory-related costs.

By modeling two different approaches—Model A and Model B—you gain deeper insight into the **cost implications of using EOQ** vs. **any custom or constrained order quantity**.

---

## 🧠 Key Concepts

| Term | Description |
|------|-------------|
| **EOQ** | Economic Order Quantity – Optimizes the balance between ordering and holding costs |
| **EPQ** | Economic Production Quantity – EOQ adjusted for in-house production with specific rates |
| **Total Relevant Cost** | Combined cost of ordering and holding inventory |
| **Prescriptive Analytics** | Recommends actions (e.g., order quantity) that minimize cost, not just predict outcomes |

---

## 🔍 Models Overview

### ✅ Model A: EOQ-Based Inventory Planning

- Calculates **EOQ** using:
  \[
  EOQ = \sqrt{\frac{2DS}{H}}
  \]
  Where:  
  - *D* = Annual demand  
  - *S* = Ordering cost per order  
  - *H* = Holding cost per unit per year

- Uses EOQ to calculate:
  - Number of orders per year
  - Time between orders
  - Total relevant cost

- Highlights the **minimum-cost theoretical order quantity**

---

### ✅ Model B: Custom Order Quantity with Solver Optimization

- Allows user to input **any order quantity** (not necessarily EOQ)
- Calculates resulting:
  - Number of orders
  - Inventory metrics
  - Total cost
- Also includes **Solver Setup**:
  - **Objective**: Minimize *Total Relevant Cost*
  - **By Changing**: Order Quantity
  - **Constraints**: 
    - Non-negative variables
  - **Solving Method**: Non-Linear

#### ⚖️ Use Cases:

1. **Compare cost of EOQ vs custom quantity**  
2. **Validate EOQ model** – Input EOQ into Model B to cross-check results  
3. **Solve real-world constraints** – Use Solver when EOQ isn’t feasible due to business or supplier restrictions

---

## 📘 EPQ Model (Optional Add-on)

- Calculates optimal **production lot size** using:
  \[
  EPQ = \sqrt{\frac{2DS}{H\left(1 - \frac{d}{p}\right)}}
  \]
  Where:
  - *d* = Demand rate
  - *p* = Production rate
- Useful for internal manufacturing environments

---

## 🛠 Tools Used

- **Microsoft Excel**
  - Custom formula modeling
  - Built-in Solver Add-in
  - Data tables for cost breakdowns
- **Analytical Techniques**
  - EOQ and EPQ formulas
  - Cost comparison
  - Optimization through Solver

---

## 📊 Visuals and Solver Settings

Solver Configuration for Model B:

- **Set Objective**: Total Relevant Cost cell
- **To**: Minimum
- **By Changing Cell**: Order Quantity
- **Check**: *Make Unconstrained Variables Non-Negative*
- **Solving Method**: Non-linear

---

## 📈 Key Insights

- EOQ helps identify the **optimal** order quantity under ideal conditions.
- Custom order quantities may lead to **higher costs**, which can be visualized in Model B.
- Solver enables **prescriptive decisions** when external constraints affect order sizing.
- Comparing both models:
  - Helps quantify **cost difference**
  - Acts as a **double-check** when same EOQ is entered into Model B

---
