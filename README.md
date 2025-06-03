## 📦 EGIER Bag Production Forecast – Scientific Computing Project

This project forecasts the monthly production of a certain type of bag at EGIER from **January 2018 to December 2033** (144 months). Using a **cubic polynomial model** and **Taylor Series approximation**, the project aims to predict production trends and determine the optimal time to begin construction of a new warehouse to avoid exceeding storage capacity.

---

### 🎯 Objectives

* Model the production trend using a polynomial regression approach.
* Use Taylor Series to numerically approximate the production model.
* Forecast when production will exceed the warehouse’s capacity of 25,000 bags.
* Recommend a start date for building a new warehouse, assuming a 13-month construction timeline.

---

### 📈 Approach & Methodology

1. **Trend Modeling**:

   * The data shows a **non-linear growth trend** that cannot be captured well by linear models.
   * A **cubic polynomial model** was chosen for its balance between flexibility and generalization.
   * Polynomial function used:

     $$
     P(x) = ax^3 + bx^2 + cx + d
     $$

     where `x` is the month index and `P(x)` is the predicted production.

2. **Insights from the Trend**:

   * Early months show **gradual production increase** due to scaling operations.
   * Later, the growth **accelerates**, likely due to increased efficiency or demand.
   * Toward the end, the growth **slows down**, indicating potential saturation.

3. **Taylor Series Approximation**:

   * Taylor expansion (centered at t=1) was used to match the cubic polynomial exactly.
   * Works well because higher-order derivatives for a cubic function (above the 3rd degree) are zero.
   * Final model is both **accurate and computationally efficient**.

---

### 🔢 Model Summary

* **Cubic Coefficients**:

  * $a = 0.004$
  * $b = -0.134$
  * $c = 47.224$
  * $d = 1748.507$
* **Approximate production at Month 100**: **8,990.562 units**

---

### 🏗️ Forecast & Recommendation

* **Warehouse capacity limit**: 25,000 bags
* **Production expected to exceed capacity**: **Month 170 (June 2032)**
* **New warehouse construction time**: 13 months
* **Recommended start of construction**: **Month 157 (May 2031)**

This timing ensures that the new warehouse will be ready before capacity is exceeded, helping avoid overflow and operational issues.
