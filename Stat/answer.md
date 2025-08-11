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


