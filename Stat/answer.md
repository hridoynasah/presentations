# Quick summary of results (assuming X = 26)

* Pearson correlation coefficient: **r = 0.9703** (strong positive correlation).
* Least-squares regression line: **ŷ = 2.4952·x + 16.9381**.
* Predicted performance for **11 GB** RAM: **ŷ ≈ 44.39**.
* Residual for the PC with **6 GB** RAM: **observed = 30**, **predicted ≈ 31.91**, **residual = 30 − 31.91 = −1.91**.
* Empirical probability that a randomly selected PC performs **more than 26**: **7/10 = 0.70 = 70%**.

---

# What I did (step-by-step, like a student)

### 1) Put the data into a table

(Performance row after substituting X = 26)

| PC | RAM (GB) | Performance |
| -: | :------: | :---------: |
|  1 |     4    |      26     |
|  2 |     8    |      34     |
|  3 |     6    |      30     |
|  4 |    16    |      58     |
|  5 |    12    |      48     |
|  6 |    10    |      41     |
|  7 |     2    | 23 (26 − 3) |
|  8 |    14    |      53     |
|  9 |     3    | 31 (26 + 5) |
| 10 |     5    |      25     |

I also produced a full table that includes predicted values and residuals (you saw this in the notebook output).

### 2) Compute means and sums (student-style)

* $\bar{x} =$ mean(RAM) = **8.000**
* $\bar{y} =$ mean(Performance) = **36.900**

Compute sums:

* $S_{xx} = \sum (x_i - \bar{x})^2 = 210.000$
* $S_{yy} = \sum (y_i - \bar{y})^2 = 1388.900$
* $S_{xy} = \sum (x_i - \bar{x})(y_i - \bar{y}) = 524.000$

### 3) Correlation coefficient

Formula: $r = \dfrac{S_{xy}}{\sqrt{S_{xx} \, S_{yy}}}$.
Plugging numbers: $r \approx 0.970256$. (Strong positive correlation.)

### 4) Fit linear regression (least squares)

Slope: $\beta_1 = \dfrac{S_{xy}}{S_{xx}} = 524 / 210 \approx 2.495238$.
Intercept: $\beta_0 = \bar{y} - \beta_1 \bar{x} \approx 16.938095$.

So the regression equation:

$$
\hat{y} = 2.4952x + 16.9381
$$

$R^2 = r^2 \approx 0.9414$ → about **94.14%** of variance in performance explained by RAM in this sample.

### 5) Prediction for 11 GB

$$
\hat{y}(11) = 2.495238\cdot 11 + 16.938095 \approx 44.386 \ (\text{rounded }44.39)
$$

### 6) Residual for PC with 6 GB

* Observed $y = 30$.
* Predicted $ \hat{y}(6) \approx 31.9095$.
* Residual = $y - \hat{y} \approx 30 - 31.9095 = -1.9095$ (≈ **−1.91**).

### 7) Scatter plot with regression line

I plotted RAM (x) vs Performance (y) and drew the fitted regression line. The plot also displays the regression equation and r / R² in the plot (you saw the image).

### 8) Probability that a randomly selected PC performs more than X (X = 26)

Counted how many PCs have performance > 26:

* Values > 26: 34, 30, 58, 48, 41, 53, 31 → 7 PCs.
* Probability (empirical) = $7/10 = 0.7 = 70\%$.



# Sattik 

Here’s the full recalculation for X = 68:


---

Quick Summary of Results

Mean RAM: 8.000

Mean Performance: 49.500

Sxx: 210.000

Syy: 2514.500

Sxy: −106.000

Pearson correlation coefficient (r): −0.1459 → weak negative correlation

R²: 0.0213 → only ~2.13% of variation explained by RAM.

Regression equation:


\hat{y} = -0.5048x + 53.5381

Residual for 6 GB: observed = 30, predicted ≈ 50.5095, residual = −20.5095

Probability performance > 68: 1/10 = 0.10 = 10%



---

Step-by-Step (Student Style)

1) Data Table

PC RAM (GB) Performance Predicted (ŷ) Residual (y − ŷ)

1 4 68 51.5190 16.4810
2 8 34 49.5000 −15.5000
3 6 30 50.5095 −20.5095
4 16 58 45.4619 12.5381
5 12 48 47.4810 0.5190
6 10 41 48.4905 −7.4905
7 2 65 52.5286 12.4714
8 14 53 46.4714 6.5286
9 3 73 52.0238 20.9762
10 5 25 51.0143 −26.0143



---

2) Means

\bar{x} = 8.000, \quad \bar{y} = 49.500


---

3) Sums of Squares

S_{xx} = 210.000, \quad S_{yy} = 2514.500, \quad S_{xy} = -106.000


---

4) Correlation

r = \frac{-106}{\sqrt{210 \cdot 2514.5}} \approx -0.1459


---

5) Regression Equation

Slope:

\beta_1 = \frac{-106}{210} \approx -0.5048

\beta_0 = 49.5 - (-0.5048)(8) \approx 53.5381

Final equation:

\hat{y} = -0.5048x + 53.5381


---

6) Prediction for 11 GB

\hat{y}(11) = -0.5048(11) + 53.5381 \approx 47.986


---

7) Residual for 6 GB

Observed: 30
Predicted:

\hat{y}(6) \approx 50.5095

30 - 50.5095 \approx -20.5095


---

8) Probability Performance > X (X = 68)

Only PC 9 has performance > 68.

P = \frac{1}{10} = 0.10 = 10\%


---

Do you want me to also explain why the correlation flipped from strongly positive to weak negative when we changed X? That’s actually pretty interesting here.

