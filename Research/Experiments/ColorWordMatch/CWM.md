---
Status: In Progress
Due: 2023-07-08
Priority: Medium
---
- [x] Use median for rxn / speed
    - [x] Compare
- [x] Re do gait metrics with avg
- [x] Gait with median
- [ ] Compare with baseline walking
- [ ] Subset of strides
- [ ] WBAM
- [ ] GRF data
- [ ]

baselineStimOff <- trimDflow(Baseline_SOff_SP_0001)  
baselineStimOn <- trimDflow(Baseline_SOn_SP_0001)

ggplot(baselineStimOff, aes(x = Time, y = LeftBelt.Speed)) +  
geom_line()

test <- baselineStimOff %>% filter(LeftBelt.Speed == 1.0) %>% pull(Time) %>% head(1)  
speed <- baselineStimOff %>% filter(Time > test) %>% pull(LeftBelt.Speed)  
speedDiff <- diff(speed)

  

  

Go over all gait metrics

[https://statsandr.com/blog/anova-in-r/#other-p-values-adjustment-methods](https://statsandr.com/blog/anova-in-r/#other-p-values-adjustment-methods)

[https://statsandr.com/blog/kruskal-wallis-test-nonparametric-version-anova/](https://statsandr.com/blog/kruskal-wallis-test-nonparametric-version-anova/)

  

All data were exported and processed in MATLAB (R2021b, MathWorks, Natick, MA, USA) and reported as mean values

±±

SD. The normality of data distributions was verified using the Kolmogorov-Smirnov normality test. For the baseline, SJTpre, and MAT, a paired samples t-test was used to compare the outcome measures between SNP conditions (i.e., active or inactive). To determine the effects of SNP on motor adaptation, a two-way repeated measures ANOVA was conducted to compare the outcome measures for each SNP condition and task (i.e., SJTpre, MAT, and SJTpost). Pair-wise post-hoc comparisons were performed using a Bonferroni adjustment. Significance was set at α < 0.05.

  

  

KS:

- H0: x and y are from same distibution if p > 0.05

  

[https://universeofdatascience.com/how-to-remove-outliers-from-data-in-r/](https://universeofdatascience.com/how-to-remove-outliers-from-data-in-r/)

  

  

PST / INT