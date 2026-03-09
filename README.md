# A/B Test Sample Size Calculation

## Project Overview

This project demonstrates how to calculate the required sample size for an A/B test designed to evaluate the impact of a pricing change on conversion rate (CVR) for an online education platform.

The hypothesis states that **reducing the price of the Premium subscription will increase the conversion rate**, compensating for the potential decrease in ARPPU and leading to an overall increase in ARPU.

The goal is to determine how many users are required **in each group (control and treatment)** to reliably detect the expected change in conversion rate.

# Business Context

An online education platform plans to run an A/B test where:

- **Control group** sees the current subscription price
- **Treatment group** sees a reduced price

The target action is a **purchase event** (course or subscription purchase).

The main metric used to evaluate the experiment is:

**Conversion Rate (CVR)**

CVR represents the proportion of users who complete the purchase action.

# Hypothesis

Reducing the price of the Premium subscription will increase the conversion rate.

Historical CVR: **0.5% (0.005)**  
Expected CVR after the change: **0.8% (0.008)**

This represents an expected relative uplift of approximately **60%**.

# Experiment Parameters

| Parameter | Value |
|--------|--------|
| Baseline Conversion Rate | 0.005 |
| Expected Conversion Rate | 0.008 |
| Significance Level (α) | 0.05 |
| Statistical Power | 0.8 |
| Test Type | Two-sided |
| Metric | Conversion Rate (purchase event) |

# Statistical Method
To estimate the required **sample size**, we use the standard formula for comparing two proportions.

$
N = \frac{(Z_{\alpha/2} + Z_{\beta})^2 \cdot \left(P_1(1-P_1) + P_2(1-P_2)\right)}{(P_2 - P_1)^2}
$

Where:

- \(P_1\) — baseline conversion rate  
- \(P_2\) — expected conversion rate  
- \(Z_{\alpha/2}\) — critical value for the significance level  
- \(Z_{\beta}\) — critical value corresponding to statistical power  

This formula estimates the **minimum number of users required per group** to detect the expected effect size with the desired statistical power.