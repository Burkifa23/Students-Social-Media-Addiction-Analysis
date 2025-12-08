### **HYPOTHESIS TEST 1: Addiction Level → Mental Health Score**

**Step 1: State the Claim**

- **Null Hypothesis (H₀):** μ_low = μ_moderate = μ_high  
  The mean mental health scores are equal across all three addiction level categories (Low, Moderate, High).

- **Alternative Hypothesis (Hₐ):** At least one μ is different  
  At least one addiction level category has a different mean mental health score than the others.

**Step 2: Collect and Summarize the Sample**

Summary Statistics by Addiction Level:
- Low addiction (1-3): Mean ≈ 8.00, SD ≈ 0.94, n = 17
- Moderate addiction (4-6): Mean ≈ 7.23, SD ≈ 1.13, n = 280
- High addiction (7-10): Mean ≈ 6.13, SD ≈ 1.41, n = 408

Total sample size: n = 705

Pattern observed: As addiction level increases from Low → Moderate → High, mean mental health scores systematically decrease, suggesting a negative association between addiction and mental health.

Conditions for one-way ANOVA:
1. ✓ Independence: Random sample, observations independent
2. ✓ Normality: Sample sizes large (n > 30 for Moderate and High groups); Low group small (n=17) but ANOVA is robust to violations with large overall sample
3. ✓ Equal variances: Standard deviations reasonably similar (ratio of largest to smallest SD < 2:1)

**Step 3: Assess the Evidence**

- Test statistic: F ≈ 109.4
- Degrees of freedom: df_between = 2, df_within = 702
- p-value < 2.2e-16 (essentially 0)
- Effect size: η² (Eta-squared) ≈ 0.238 (23.8% of variance in mental health explained by addiction level)

**Step 4: Make a Conclusion**

Decision Rule: Reject H₀ if p-value < α = 0.05

Conclusion: Since p-value < 0.001, we reject the null hypothesis. There is extremely strong statistical evidence that mean mental health scores differ significantly across addiction levels. The systematic pattern (Low: 8.00 → Moderate: 7.23 → High: 6.13) indicates that higher addiction levels are associated with substantially lower mental health scores. The effect size of η² = 0.238 is considered large by conventional standards (small: 0.01, medium: 0.06, large: 0.14), indicating that addiction level is a meaningful predictor of mental health outcomes.

**Type of Error:** Because we rejected the null hypothesis, we could have made a **Type I error** (false positive). This would mean concluding that mental health differs across addiction levels when in reality there is no difference in the population. However, given the extremely small p-value and large effect size, this is highly unlikely.

**Post-hoc Test: Tukey HSD (Honestly Significant Difference)**

Since the null hypothesis was rejected and there are more than two groups, a Tukey HSD post-hoc test was conducted to determine which specific pairs of addiction levels differ significantly:

Results (all comparisons at α = 0.05):
- **Moderate vs. Low**: Mean difference ≈ -0.77, p < 0.05 (significant)  
  Students with moderate addiction score about 0.77 points lower on mental health than those with low addiction.

- **High vs. Low**: Mean difference ≈ -1.87, p < 0.001 (significant)  
  Students with high addiction score about 1.87 points lower on mental health than those with low addiction.

- **High vs. Moderate**: Mean difference ≈ -1.10, p < 0.001 (significant)  
  Students with high addiction score about 1.10 points lower on mental health than those with moderate addiction.

Interpretation: All three pairwise comparisons are statistically significant. Each increase in addiction category (Low → Moderate → High) is associated with a statistically significant and practically meaningful decrease in mental health scores. The largest difference is between Low and High addiction groups (1.87 points on the 10-point scale), representing a substantial deterioration in mental health associated with high addiction levels.

---

### **HYPOTHESIS TEST 2: Addiction Score → Relationship Conflicts**

**Step 1: State the Claim**

- **Null Hypothesis (H₀):** ρ = 0  
  There is no linear relationship between addiction score and relationship conflicts in the population (correlation is zero).

- **Alternative Hypothesis (Hₐ):** ρ ≠ 0  
  There is a linear relationship between addiction score and relationship conflicts in the population (correlation is not zero).

**Step 2: Collect and Summarize the Sample**

Summary Statistics:
- Addiction Score: Mean = 6.44, SD = 1.59
- Relationship Conflicts: Mean = 2.85, SD = 0.96
- Sample size: n = 705
- Sample correlation: r = 0.934

Conditions for Pearson correlation test:
1. ✓ Linear relationship: Scatterplot shows strong linear pattern
2. ✓ No extreme outliers: Data well-distributed along line
3. ✓ Independence: Observations are independent
4. ✓ Large sample size (n > 30)

**Step 3: Assess the Evidence**

- Correlation coefficient: r = 0.934
- R² = 0.872 (87.2% of variance in conflicts explained by addiction score)
- Test statistic: t = 82.61
- Degrees of freedom: df = 703
- p-value < 2.2e-16 (essentially 0)

**Step 4: Make a Conclusion**

Decision Rule: Reject H₀ if p-value < α = 0.05

Conclusion: Since p-value < 0.001, we reject the null hypothesis. There is extremely strong statistical evidence of a positive linear relationship between addiction score and relationship conflicts. The correlation of r = 0.934 indicates a very strong positive association—as addiction scores increase, the number of relationship conflicts increases substantially.

**Type of Error:** Because we rejected the null hypothesis, we could have made a **Type I error** (false positive). However, with such an extremely small p-value and very high correlation, this is highly unlikely.

**Post-hoc Test: Regression Slope Interpretation**

Linear regression equation: Conflicts = -0.772 + 0.563 × Addiction_Score

Interpretation: For each 1-point increase in addiction score, the number of relationship conflicts increases by approximately 0.56 conflicts on average. This is a substantial practical effect—a student moving from low addiction (score 3) to high addiction (score 8) would be predicted to experience approximately 2.8 more conflicts (5 × 0.56).

---

### **HYPOTHESIS TEST 3: Usage Category → Academic Performance**

**Step 1: State the Claim**

- **Null Hypothesis (H₀):** Usage category and academic performance impact are independent  
  There is no association between social media usage category and whether students report negative academic impact.

- **Alternative Hypothesis (Hₐ):** Usage category and academic performance impact are not independent  
  There is an association between social media usage category and whether students report negative academic impact.

**Step 2: Collect and Summarize the Sample**

Sample Proportions (reporting "Yes" - negative impact):
- Moderate usage (2-4h): 15.6% (26/167)
- High usage (4-6h): 72.3% (284/393)
- Very high usage (6+h): 100% (143/143)

Total sample size: n = 703 (excluding Low usage category with n=2)

Contingency Table:
```
                    No    Yes
Moderate (2-4h)    141     26
High (4-6h)        109    284
Very High (6+h)      0    143
```

Conditions for chi-square test:
1. ✓ Independence: Observations are independent
2. ✓ Expected frequencies: All expected counts > 5 (minimum = 50.85)
3. ✓ Random sample from population

**Step 3: Assess the Evidence**

- Chi-square test statistic: χ² = 263.47
- Degrees of freedom: df = 2
- p-value = 6.15 × 10⁻⁵⁸ (essentially 0)
- Effect size: Cramér's V = 0.612 (large effect)

**Step 4: Make a Conclusion**

Decision Rule: Reject H₀ if p-value < α = 0.05

Conclusion: Since p-value < 0.001, we reject the null hypothesis. There is extremely strong statistical evidence of an association between social media usage category and academic performance impact. Students in higher usage categories are substantially more likely to report that social media negatively affects their academic performance. The effect size (Cramér's V = 0.612) indicates a large practical significance (V > 0.5 is considered large).

The pattern is striking: only 15.6% of moderate users report negative impact, but this jumps to 72.3% for high users and reaches 100% for very high users. This monotonic relationship suggests not just statistical association but a clear dose-response pattern where increased usage progressively increases the likelihood of academic problems.

**Type of Error:** Because we rejected the null hypothesis, we could have made a **Type I error** (false positive). However, the extremely small p-value makes this highly unlikely.

**Post-hoc Test:** The pattern is clear and monotonic: as usage increases from Moderate → High → Very High, the proportion reporting negative academic impact increases dramatically (15.6% → 72.3% → 100%). Given the large sample sizes and dramatic differences in proportions, all pairwise comparisons would be statistically significant. The zero count in the "Very High/No" cell is particularly noteworthy—literally 100% of students using social media 6+ hours daily report academic problems, suggesting this usage level is incompatible with academic success.








