# Statistical Quality Control and Regression Analysis for Manufacturing Process Assessment

---

## Table of Contents
- Overview
- Problem Context
- Statistical Quality Control (SQC)
  - Large-Group Descriptive Analysis
  - Subgroup Perspective & Rational Subgrouping
  - X̄–S Control Chart Construction
  - Sigma Zones & Western Electric Rules
  - Process Stability Assessment
- Simple Linear Regression
  - Exploratory Data Analysis
  - Model Formulation & Estimation
  - Statistical Inference
  - Model Diagnostics
  - Prediction & Extrapolation Risks
- Key Takeaways
- Academic Context

---

## Overview

This assessment analyzes two distinct but complementary statistical problems:

1. **Quality Control of a Manufacturing Process**  
   Using control charts to determine whether a water-resistance process is statistically stable and predictable.

2. **Regression Modeling of Physical Data**  
   Modeling the relationship between temperature and thermal conductivity using simple linear regression, followed by inference, diagnostics, and prediction analysis.

All mathematical derivations, intermediate steps, and computations are provided in the PDF report, while this README focuses on **methodology, reasoning, and conclusions**.

---

## Problem Context

### Statistical Quality Control
- Dataset: 30 water-resistance measurements
- Structure: 10 rational subgroups, each of size 3
- Objective: Determine whether observed variability is due to **common causes** or **special causes**

### Regression Analysis
- Dataset: 10 paired observations of temperature (°F) and thermal conductivity
- Objective: Quantify the strength, direction, and reliability of the linear relationship between variables

---

## Statistical Quality Control (SQC)

### Large-Group Descriptive Analysis

**How it was performed:**
- All 30 measurements were treated as a single dataset.
- Summary statistics were computed, including mean, median, variance, standard deviation, range, and quartiles.
- Distribution shape was visually evaluated using a histogram and boxplot.

**Purpose:**
- To understand the overall distribution of the process output.
- To assess central tendency, spread, skewness, and presence of outliers.

**Result:**
The process output is centered around 30 units with moderate variability and no extreme outliers. However, this approach does not capture how the process behaves over time.

---

### Subgroup Perspective & Rational Subgrouping

**How it was performed:**
- Measurements were organized into 10 rational subgroups of size 3.
- Each subgroup represents observations taken under similar conditions and short time intervals.
- Subgroup means and subgroup standard deviations were computed.

**Purpose:**
- To separate short-term (within-group) variation from long-term (between-group) variation.
- To enable time-based monitoring of the process.

**Result:**
Subgroup statistics provided the foundation for control chart construction and process stability evaluation.

---

### X̄–S Control Chart Construction

**How it was performed:**
- The grand mean of subgroup means and the average subgroup standard deviation were calculated.
- X̄ and S control charts were constructed using Shewhart constants appropriate for subgroup size.
- 3σ control limits were established for both charts.

**Purpose:**
- The X̄ chart monitors shifts in the process mean.
- The S chart monitors changes in within-subgroup variability.

**Result:**
All subgroup means and standard deviations fell within their respective control limits.

---

### Sigma Zones & Western Electric Rules

**How it was performed:**
- 2σ warning limits were calculated.
- Sigma zones (A, B, and C) were defined on the X̄ chart.
- Western Electric rules were evaluated to detect non-random patterns, including runs, trends, and clustering.

**Purpose:**
- To detect early signs of process instability before a full control limit violation occurs.

**Result:**
No Western Electric rules were violated, and no abnormal patterns were detected.

---

### Process Stability Assessment

**Final SQC Conclusion:**
The water-resistance manufacturing process is **statistically stable and in control**, with observed variability consistent with common causes inherent to the current process design.

This stability implies predictability but does not automatically guarantee conformance to customer specifications.

---

## Simple Linear Regression

### Exploratory Data Analysis

**How it was performed:**
- Means and standard deviations were computed for both variables.
- A scatterplot was used to visualize the relationship between temperature and conductivity.

**Purpose:**
- To assess linearity and justify fitting a regression model.

**Result:**
A strong positive linear relationship was observed.

---

### Model Formulation & Estimation

**How it was performed:**
- A simple linear regression model was defined.
- Model parameters (slope and intercept) were estimated using the Ordinary Least Squares method.

**Purpose:**
- To quantify how changes in temperature affect thermal conductivity.

**Result:**
The fitted model indicates that conductivity increases by approximately **11.15 units per 1°F increase in temperature**.

---

### Statistical Inference

**How it was performed:**
- Residual standard error was computed using the sum of squared errors.
- Hypothesis tests were conducted for both regression coefficients.
- The coefficient of determination (R²) was calculated.

**Result:**
Both coefficients were highly statistically significant, and the model explained approximately **98% of the variability** in thermal conductivity.

---

### Model Diagnostics

**How it was performed:**
- Residuals vs. fitted values were analyzed to assess linearity and constant variance.
- A normal Q–Q plot was used to evaluate residual normality.

**Result:**
No major violations of regression assumptions were detected, supporting valid inference within the observed data range.

---

### Prediction & Extrapolation Risks

**How it was performed:**
- Point prediction, confidence interval, and prediction interval were computed at −10°F.

**Result:**
All predictions at −10°F were physically impossible (negative conductivity), demonstrating that:
- The model is reliable for **interpolation** within the observed range.
- The model is **unsafe for extrapolation** beyond that range.

---

## Key Takeaways

- Control charts are essential for distinguishing common-cause from special-cause variation.
- A stable process is predictable but must still be compared to specification limits.
- Regression models can fit data extremely well yet fail when extrapolated beyond physical constraints.
- Statistical models must always be interpreted alongside domain knowledge.
