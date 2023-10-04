
# Automaticity 

COM: lateral usually decreases for better stability as speed increases
- May indicate more automatic spinal level of control , bypassing cerebellum/vestibular input 
Bow tie becomes more U shaped, increasing in z 

Tesio 
```
The mechanical role of plantar flexors seems crucial, given that they are synchronous with the a increment of Etot, which is 3 to 4 times higher than the b increment at all velocities (Figure 8A) (20). In the asymmetric impairment caused by above- or below-knee amputation, the a increment is increased when the unaffected limb is trailing (N/P transition in Figure 8B); correspondingly, the plantar flexors may generate a peak power 3 times higher, compared to the next a increment sustained by the muscles of the amputated limb (P/N transition in Figure 8B) (66).
```

# NEC Data Synthesis

LE02;
- GRF: mix of PST and INT effects
- 

LE04:
-  GRF: mix of PST and INT effects

LE06:
- GRF
	- No SNP effects, few with stim type
	- Only on INT 

All Stimulus effect on INT min Y force (breaking)
- Decrease for LE02/6, increase for 4
- less cautious, speed up and increase maintaining steady gait

Stride Time By leg
Average
- LE06 pst + int SNp
- LE02 int Stimulus Type decrease with difficulty 
-COV
- LE02 pST snp
Sd
- LE02 pst SNP

Stance Time by leg
- LE02: greater times for easier, both legs
- As task gets harder, less time in stance

# GL
CoM 3D
Margin of stability 
GRF over gait cycle 
# GRF
LE02: PST = R
LE04: PST = R
LE06: PST = L

GRF: + values for x = outward 

LHS = green
LTO = red
RHS = blue
RTO = orange

  # Remove from raw gait data
  outliersRawGrf <- switch(i,NULL, NULL, c(5961:6026, 6270:6329, 8569:8630), NULL, NULL, c(5719:5780, 6035:6097))


Old remove outliers 
dim(GRF_L)[1] - length(outliersRawGrf)

    originalGrfL <- GRF_L
  originalGrfR <- GRF_R
  GRF_L[-outliersRawGrf,] <-  data.frame(matrix(NA,    # Create empty data frame
                          nrow = length(GRF_L) - length(outliersRawGrf),
                          ncol = 3))
  GRF_R[-outliersRawGrf,] <- data.frame(matrix(NA,    # Create empty data frame
                          nrow = length(GRF_R) - length(outliersRawGrf),
                          ncol = 3))
  
  gaitMetricsAll <- computeGaitMetrics(1, gaitEventsL, gaitEventsR, trialData, 
                                       trialExtract, heelDif)
# Other Metrics
CoM range (cm)
e local dynamic stability (Lyapunov exponents, ask Suzhou. He dealt with it in the previous journal club). You may also need to check simple stride-to-stride variability (both spatial and temporal, see the paper from hausdorff). I think I shared you his paper before.


# Off by one error 8/27

Removing line 17593

![[Untitled 627.png]]

Correct event log so missing C corresponds to the line with time 87.12333 instead of a null value

![[Untitled 628.png]]

# DK 7/10

LE02

Initial 5 steps and last 5 steps

30 strides

Outliers :

Le01 showed long stance times

Find outliers: look at GRF plot

- find outliers , remove
- remove outliers from baseline,
- gait is variable, outliers matter

Self paced???

- not a huge difference in sp

Consistency between steps and sessions

- LE02 with increasing speed should show consistency wit other fair parameters.
- parameters should support each other
- cross check data
- explain why there's nothing

Normalize Grf from static trial

Braking force should be negative

- **negative force breaking force first HS, propulsive toe off**
- GRF Y should be flipped. GRF X for the right foot should be flipped.
- Positive x to the right 

Grabbing the bar

How to normalize wbam

- way to normalize variable , stide speed
- 30 strides: 30 WBAM, 30 speeds

Speed:

- start with walking speed differences in story
- why speed up with task difficult? Cognitive task not that difficulty

Prioritizing cognitive task

- may not be paying attention to feedback

Proof that task is difficult, RT for IC goes up

WBAM

Consistent sit in frontal plane angular momentum SNP on and off

- lots of outliers
- should be consistent
- each stride whole body angular momentum is conserved
- dynamic balance
- SD should be small
- mean value should be similar

Symmetry and stability

- stride variability

Step symmetry and stability : dual tasking may affect gait stability, snp may have positive impact

  

- [ ] Remove grf outliers
- [ ] normalize wbam by variable speed
- [x] take middle strides for all metrics

# Compare with DK

'COP_FP1.txt'  
'COP_FP2.txt'  
'GRF_FP1.txt'  
'GRF_FP2.txt'  
'GRM_FP1.txt'  
'GRM_FP2.txt'  
'LANK.txt'  
'LFT_CGPos.txt'  
'LFT_CGVel.txt'  
'LHEE.txt'  
'LSK_CGPos.txt'  
'LSK_CGVel.txt'  
'LTH_CGPos.txt'  
'LTH_CGVel.txt'  
'LTOE.txt'  
'L_Ankle_Angle.txt'  
'L_Ankle_Moment.txt'  
'L_Ankle_Power.txt'  
'L_Hip_Angle.txt'  
'L_Hip_Moment.txt'  
'L_Hip_Power.txt'  
'L_Knee_Angle.txt'  
'L_Knee_Moment.txt'  
'L_Knee_Power.txt'  
'RANK.txt'  
'RFT_CGPos.txt'  
'RFT_CGVel.txt'  
'RHEE.txt'  
'RSK_CGPos.txt'  
'RSK_CGVel.txt'  
'RTH_CGPos.txt'  
'RTH_CGVel.txt'  
'RTOE.txt'  
'R_Ankle_Angle.txt'  
'R_Ankle_Moment.txt'  
'R_Ankle_Power.txt'  
'R_Hip_Angle.txt'  
'R_Hip_Moment.txt'  
'R_Hip_Power.txt'  
'R_Knee_Angle.txt'  
'R_Knee_Moment.txt'  
'R_Knee_Power.txt'  
'WB_AM.txt'  
'WB_COM_DIST.txt'

  

# Gait

![[Untitled 629.png]]

**Figure from: Stöckel, Tino & Jacksteit, Robert & Behrens, Martin & Skripitz, Ralf & Bader, Rainer & Mau-Moeller, Anett. (2015). The mental representation of the human gait in young and older adults. Frontiers in Psychology. 6. 943. 10.3389/fpsyg.2015.00943.**

**Perry, J., and Burnﬁeld, J. M. (2010). Gait Analysis: Normal and Pathological Function. New York, NY: Slack Inc**

  

# BUGS

## Max Number of GRF Frames - Fixed

GRF_L x,y,z max = 11065

gaitEventsR heel strike max element: 10995

  

Solution: should be used indexCycleStart and End to extract values from GRF not the frame start and end

## Subsetting - Fixed

Turned out to be issue above

![[Untitled 630.png]]

Subset should be 3487 but using xilm or scale x cont it subsets at 5 when no 5 is being passed in at all???

X is shifted but y isn’t

  

MUST USE row names to subset by row index in xlim

```
testPlot<- ggplot(data = GRF_L) +   geom_line( aes(x = as.numeric(row.names(GRF_L)), y = -x), color = "blue") +  geom_line(aes(x = as.numeric(row.names(GRF_L)), y = -y), color = "red") +  geom_line( aes(x = as.numeric(row.names(GRF_L)), y = z), color = "black") +  # geom_line(data = GRF_R, aes(x = frameTime$Frame, y = -x),  #           linetype = "dashed", color = "blue") +  # geom_line(data = GRF_R, aes(x = frameTime$Frame, y = -y), linetype = "dashed",  #           color = "red",) +  # geom_line(data = GRF_R, aes(x = frameTime$Frame, y = z), linetype = "dashed",  #           color = "black") +  xlim(frameStart,frameEnd) +  ylim(-100, 800) +   geom_hline(yintercept = 763)  plotData <- ggplot_build(testPlot)view(plotData$data[[3]])
```

# Gait Cycle

![[Untitled 631.png]]

![[Untitled 632.png]]

  

# Axes

  

![[Untitled 633.png]]

Flip the axis of the y data for anterior posterior to be correct

![[Untitled 634.png]]

  

![[Untitled 635.png]]

  

  

# Hamid 5/5

![[Untitled 636.png]]

  

  

```
mod <- glm(Errors ~ View + SNP + Evaluation + View*Evaluation + SNP*Evaluation, data= ErrorData
```

Multiple Comparisons Problem

- More inferences = higher chance of errors: more likely that when comparing many attributes at least one will have some significant difference

[https://aosmith.rbind.io/2019/03/25/getting-started-with-emmeans/#the-dataset-and-model](https://aosmith.rbind.io/2019/03/25/getting-started-with-emmeans/#the-dataset-and-model)

[https://www.r-bloggers.com/2020/04/estimating-and-testing-glms-with-emmeans/](https://www.r-bloggers.com/2020/04/estimating-and-testing-glms-with-emmeans/)

[https://www.youtube.com/watch?v=_okuMw4JFfU](https://www.youtube.com/watch?v=_okuMw4JFfU)

  

To use the Generalized Linear Model (GLM) for data with two groups and three condition types and perform post hoc tests on the significant interactions, you can follow these steps:

Step 1: Load the necessary package

```
library(stats)
```

Step 2: Fit the GLM model with interaction terms  
Assuming you have your data loaded and formatted appropriately, fit the GLM model with interaction terms using the `glm()` function.

```
model <- glm(response_variable ~ group * condition, data = your_data, family = gaussian)
```

Replace `response_variable`, `group`, `condition`, and `your_data` with the appropriate variable names from your dataset. The `family` argument is set to `"gaussian"` for continuous response variables. Adjust it accordingly if you have a different response type.

Step 3: Perform the post hoc tests on significant interactions  
To perform the post hoc tests on the significant interactions, you can use the `emmeans` package. First, install the package using the `install.packages()` function if it is not already installed.

```
install.packages("emmeans")
```

After installing the `emmeans` package, load it into your R session.

```
library(emmeans)
```

Next, use the `emmeans()` function to calculate the estimated marginal means and perform the post hoc tests on the significant interactions.

```
em <- emmeans(model, pairwise ~ group:condition)# View the estimated marginal meansprint(em)# Perform post hoc testsposthoc_results <- pairs(em)# View the post hoc test resultsprint(posthoc_results)
```

The `emmeans()` function is used to calculate the estimated marginal means for each combination of the `group` and `condition` factors. The `pairwise ~ group:condition` argument specifies that pairwise comparisons should be performed for the interaction between `group` and `condition`.

The `pairs()` function is then used to perform the post hoc tests on the estimated marginal means. The results are stored in the `posthoc_results` object.

Finally, you can print the `em` object to view the estimated marginal means and the `posthoc_results` object to view the post hoc test results.

Please note that the code provided assumes a Gaussian family and continuous response variables. If you have different assumptions or requirements (e.g., different families or non-parametric tests), you may need to adjust the code accordingly.

Remember to install any required packages using the `install.packages()` function before loading them with `library()`.

  

EMM

Estimated marginal means (EMMs) are a statistical concept used in the analysis of data to estimate the average response or outcome for different levels or combinations of independent variables. EMMs are particularly useful when there are multiple independent variables or when interactions between variables are present.

In many statistical models, the estimated coefficients represent the average effects of the independent variables on the dependent variable, assuming all other variables are held constant. However, when there are interactions between variables, the interpretation of the coefficients becomes more complex. EMMs help to overcome this issue by providing estimated means for specific combinations of variables, while taking into account the interactions.

EMMs are estimated using statistical techniques such as linear regression, analysis of variance (ANOVA), or generalized linear models. These techniques allow researchers to estimate the average response for each combination of independent variables, while controlling for other variables in the model. The estimated means provide a clearer understanding of the relationship between the independent variables and the dependent variable.

EMMs are often used in fields such as social sciences, psychology, economics, and biology, where researchers are interested in understanding the effects of multiple variables on a particular outcome. They allow for more nuanced interpretations of the results and help researchers make comparisons between different levels or combinations of variables.

Overall, estimated marginal means provide a way to estimate and interpret average responses for different combinations of independent variables, considering the interactions between them. They are a valuable tool in statistical analysis for understanding the relationships and effects of variables on an outcome of interest.

  

What sign EMM means

When an estimated marginal mean is statistically significant, it means that there is a significant difference between the means of the groups or conditions being compared. In other words, the observed difference in means is unlikely to have occurred by chance alone and is likely to reflect a true difference in the population.

Estimated marginal means (also known as least-squares means) are adjusted means that take into account the effects of other variables in the model. They provide a way to estimate the mean response for each group or condition, while controlling for the effects of other factors.

When the estimated marginal mean for a particular group or condition is significant, it indicates that there is evidence to suggest that the mean response for that group or condition is different from the reference group or condition. The significance level (often denoted by p-value) associated with the estimated marginal mean provides a measure of the strength of evidence against the null hypothesis of no difference.

It's important to note that statistical significance alone does not necessarily imply practical or meaningful significance. Effect size and the context of the study should also be considered when interpreting the significance of estimated marginal means.

# General

Event B = StopwatchStart: main stopwatch for next word trigger

Event C = Next work: triggered by click

  

  

LE01 combined

![[Untitled 637.png]]

LE01 combined speed

![[Untitled 638.png]]

# 3/22 Statistical Consulting

Overview of Exp

Main Questions

- Is the Wilcoxon test the best for comparing the means of the reaction speed and treadmill data?
    - [http://rpkgs.datanovia.com/ggpubr/reference/compare_means.html](http://rpkgs.datanovia.com/ggpubr/reference/compare_means.html)
    - [https://rdrr.io/r/stats/wilcox.test.html](https://rdrr.io/r/stats/wilcox.test.html)
- How to determine the interaction between different conditions to see if data can be lumped
- Statistical test to determine difference in accuracy percentage scores?
    - Paired t-test

  

Paired t-test:

- Decide what baseline and what comparing to
- T-test

  

Power to detect anything

Look at describing effect size

- Descriptive in nature
- Base on this, dramatic difference or not

  

Gait, reaction time to stimuli

  

  

Difference in means: is normally distributed

- Normal distrbution of extracted values

  

Normal

- Frequency on variable
- Skewness of 3 to -3
- kurtosis: 8 to -8

  

Paired t-test

  

p-value is significant : transforming it isn’t going to add more significance

- P less than 0.1 or 0.105 maybe might get something

  

Report effect size: medium to large

- With a larger sample, something noticeable

  

SPS versions on MyApps

- Data has to be wide vs long , one data row per person

  

standard deviation of differences to estiamte effect size

SPSS: ananlyse, compare means, expecting medium effect size

- detectable to the human eye, average of all tests

  

Cohens d to get effect size

  

Baseline stim

  

Total works and separate which ever is better

  

Effect sizes useful for future studies

  

Paired t-test: bon feroni adjustments, protect against a fishing expededition

- Start including a hypothesis don’t have that issue
- Hyptohosis on logic, theory, or prior empirical evidence

  

Keep an eye out for the HW, otherwise shoot email by next week

mod <- glm(Errors ~ View + SNP + Evaluation + View_Evaluation + SNP_Evaluation, data= ErrorData