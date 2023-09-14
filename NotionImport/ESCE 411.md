---
Priority: Today
Area: School
Status: Done
---
- [x] Final project proposal
- [ ] Lectures M10
- [ ] Lectures M11
- [ ] Final project

Videos

- M11 Linear Regression: [**https://youtu.be/foMb97s_zzY**](https://youtu.be/foMb97s_zzY) **,** [**https://youtu.be/2cPDxXrgghQ**](https://youtu.be/2cPDxXrgghQ)
- Mulitple LIenar Regression [**https://youtu.be/-LqTJGgGVgc**](https://youtu.be/-LqTJGgGVgc) **,** [**https://youtu.be/jylBK7U4hsc**](https://youtu.be/jylBK7U4hsc)
- Analysis of Variance: [**https://youtu.be/haaWHitXsW8**](https://youtu.be/haaWHitXsW8)**,** [**https://youtu.be/y6ZtMFauurg**](https://youtu.be/y6ZtMFauurg)
- Module 14 Factorial Desing [https://youtu.be/hFTWvo5avpU](https://youtu.be/hFTWvo5avpU)

  

[https://doi.org/10.3389%2Ffnsys.2013.00041](https://doi.org/10.3389%2Ffnsys.2013.00041)

  

  

---

## title: "ECS411 Final Project"  
author: "Eileen Petros"  
date: "`r format(Sys.time(), '%d %B, %Y')`"  
output:  
pdf_document:  
toc: true  
toc_depth: 3  
df_print: kable

# Setup

```
knitr::opts_chunk$set(echo = TRUE)library(tidyverse)library(ggpubr)library(rstatix)library(moments)options(knitr.table.format = "latex")
```

# Functions

```
ALPHA <- 0.05physioData <- function(metricString){  lowMetric <- lowDf %>% pull(metricString)  highMetric <- highDf %>% pull(metricString)  # Not norrmal, but enough observations  # skewness(lowMetric)  # kurtosis(lowMetric)  test <- t.test(x = lowMetric, y = highMetric, paired = FALSE, conf.level = 0.95)  test2 <- var.test(x = lowMetric, y = highMetric, paired = FALSE, conf.level = 0.95)  lowMean <- mean(lowMetric, na.rm = TRUE)  highMean <- mean(highMetric, na.rm = TRUE)  lowVar <- var(lowMetric, na.rm = TRUE)  highVar <- var(highMetric, na.rm = TRUE)  metrics <<- c(metrics, metricString)  lowMeans <<- c(lowMeans, lowMean)  highMeans <<- c(highMeans, highMean)  lowVars <<- c(lowVars, lowVar)  highVars <<- c(highVars, highVar)  pValuesMean <<- c(pValuesMean, test$p.value)  pValuesVar <<- c(pValuesVar, test2$p.value)  # print(lowMean)  # print(highMean)  # print(lowVar)  # print(highVar)  means <- c(mean(lowMetric), mean(highMetric))  vars <- c(var(lowMetric), var(highMetric))  # table <- table %>% bind_cols(metricString = c(means, vars))  # test$p.value < ALPHA}presenceQData <- function(video1, video2){  x <- longRaw %>% select(-metric) %>% filter(Num_Code == video1) %>% pull(value)  y <- longRaw %>% select(-metric) %>% filter(Num_Code == video2) %>% pull(value)  print(t.test(x = x, y = y, paired = FALSE, conf.level = 0.95))  print(var.test(x, y))}
```

# Data Import

```
# rawData <- read.table("./VREED/03 Self-Reported Questionnaires/01 Participant Profile  Pre-Exposure Ratings.xlsx",#                       sep = "\\t", header = TRUE, fileEncoding = "UTF-8", skipNul = TRUE)videos <- read.csv("./VREED/02 Stimuli Selection/02 Final Videos Description.csv", na.strings = "")partcipantDataPreExposure <- read.csv("./VREED/03 Self-Reported Questionnaires/01 Participant Profile  Pre-Exposure Ratings.csv")postExposure <- read.csv("./VREED/03 Self-Reported Questionnaires/02 Post Exposure Ratings.csv")eyeTracking <- read.csv("./VREED/04 Eye Tracking Data/02 Eye Tracking Data (Features Extracted)/EyeTracking_FeaturesExtracted.csv")ecg <- read.csv("./VREED/05 ECG-GSR Data/02 ECG-GSR (Features Extracted)/ECG_FeaturesExtracted.csv")gsr <- read.csv("./VREED/05 ECG-GSR Data/02 ECG-GSR (Features Extracted)/GSR_FeaturesExtracted.csv")
```

# Data Clean

```
# Contains multiple trials, each num code occurs 34 times once for each participant# postExposure <- postExposure %>% filter(complete.cases(postExposure))# test <- postExposure %>% filter(Trial_Num == 1) %>% select(-Trial_Num) %>%  # group_by(Num_Code) %>% summarise(across(starts_with("POST_PQ")), mean)  # summarise(across(c(2:6,8:27), mean))# group_by(ID, Num_Code) %>%# select(-Trial_Num, -ID) %>%  summarise_if(is.numeric, mean)# postExposure <- postExposure %>% filter(complete.cases(postExposure))videos <- videos %>% fill(Video_ID, Brief_Title, Brief_.Description, Quad_Cat, Arousal_Cat, Valence_Cat, Str_Code, Num_Code, Channel.Artist, Video_Link, Video_Length, Notes_on_Length)exposure <- left_join(partcipantDataPreExposure, postExposure)
```

```
videoCodes <- videos %>% select(Num_Code, Brief_Title,Quad_Cat) %>% unique()
```

# Fear Ratings

```
fearRatings <- exposure %>% select(Num_Code, PRE_Fear, POST_Fear) %>%  mutate(normalizedRating = POST_Fear - PRE_Fear)meanFearRatings <- fearRatings %>% group_by(Num_Code) %>%  summarise(mean = mean(normalizedRating, na.rm = TRUE)) %>% arrange(mean)lowFearVids <- meanFearRatings %>% head(1)highFearVids <- meanFearRatings %>% tail(1)videoCodes %>% filter(Num_Code %in% lowFearVids$Num_Code)videoCodes %>% filter(Num_Code %in% highFearVids$Num_Code)
```

# Joy Ratings

```
joyRatings <- exposure %>% select(Num_Code, PRE_Joy, POST_Joy) %>%  mutate(normalizedRating = POST_Joy - PRE_Joy)meanJoyRatings <- joyRatings %>% group_by(Num_Code) %>%  summarise(mean = mean(normalizedRating, na.rm = TRUE)) %>% arrange(mean)lowJoyVids <- meanJoyRatings %>% head(1)highJoyVids <- meanJoyRatings %>% tail(1)videoCodes %>% filter(Num_Code %in% lowJoyVids$Num_Code)videoCodes %>% filter(Num_Code %in% highJoyVids$Num_Code)
```

# Anger Ratings

```
angerRatings <- exposure %>% select(Num_Code, PRE_Anger, POST_Anger) %>%  mutate(normalizedRating = POST_Anger - PRE_Anger)meanAngerRatings <- angerRatings %>% group_by(Num_Code) %>%  summarise(mean = mean(normalizedRating, na.rm = TRUE)) %>% arrange(mean)lowAngerVids <- meanAngerRatings %>% head(1)highAngerVids <- meanAngerRatings %>% tail(1)videoCodes %>% filter(Num_Code %in% lowAngerVids$Num_Code)videoCodes %>% filter(Num_Code %in% highAngerVids$Num_Code)
```

```
angerRatings <- exposure %>% select(Num_Code, PRE_Anxiousness, POST_Anxiousness) %>%  mutate(normalizedRating = POST_Anxiousness - PRE_Anxiousness)meanAngerRatings <- angerRatings %>% group_by(Num_Code) %>%  summarise(mean = mean(normalizedRating, na.rm = TRUE)) %>% arrange(mean)lowAngerVids <- meanAngerRatings %>% head(1)highAngerVids <- meanAngerRatings %>% tail(1)videoCodes %>% filter(Num_Code %in% lowAngerVids$Num_Code)videoCodes %>% filter(Num_Code %in% highAngerVids$Num_Code)
```

All high fear videos are contained in the second quadrant category.

# Eye Tracking for Low / High Fear Videos

```
highFearEyeTracking <- eyeTracking %>% filter(Quad_Cat == 3)lowFearEyeTracking <- eyeTracking %>% filter(Quad_Cat == 1)lowDf <- lowFearEyeTrackinghighDf <- highFearEyeTrackingmetrics <- c()lowMeans <- c()highMeans <- c()lowVars <- c()highVars <- c()pValuesMean <- c()pValuesVar <- c()physioData("Num_of_Blink")physioData("Num_of_Saccade")physioData("Mean_Fixation_Duration")physioData("Mean_Saccade_Duration")physioData("Mean_Saccade_Amplitude")physioData("Mean_Saccade_Length")physioData("Mean_Blink_Duration")eyeTrackingResults <- cbind( metrics, lowMeans, highMeans, pValuesMean,                             lowVars,highVars, pValuesVar)data.frame(eyeTrackingResults)
```

# ECG for Low / High Videos

```
lowFearECG <- ecg %>% filter(Quad_Cat == 0)highFearECG <- ecg %>% filter(Quad_Cat == 2)lowDf <- lowFearECGhighDf <- highFearECGmetrics <- c()lowMeans <- c()highMeans <- c()lowVars <- c()highVars <- c()pValuesMean <- c()pValuesVar <- c()physioData("Bpm")ecgResults <- cbind( metrics, lowMeans, highMeans, pValuesMean,                     lowVars,highVars, pValuesVar)data.frame(ecgResults)
```

# GSR for Low / High Videos

```
lowFearGSR <- gsr %>% filter(Quad_Cat == 0)highFearGSR <- gsr %>% filter(Quad_Cat == 2)metrics <- c()lowMeans <- c()highMeans <- c()lowVars <- c()highVars <- c()pValuesMean <- c()pValuesVar <- c()lowDf <- lowFearGSRhighDf <- highFearGSRphysioData("Mean")gsrResults <- cbind( metrics, lowMeans, highMeans, pValuesMean,                     lowVars,highVars, pValuesVar)data.frame(gsrResults)
```

# Presence Questionaire

```
presenceQ <- exposure %>% select(Num_Code,Quad_Cat, matches("POST_PQ+\\\\d"))presenceQ <- presenceQ %>% group_by(Num_Code) %>%  summarise_if(is.numeric, mean, na.rm = TRUE)lowFearPQ <- presenceQ %>% filter(Quad_Cat == 1)highFearPQ <- presenceQ %>% filter(Quad_Cat == 3)lowDf <- lowFearPQhighDf <- highFearPQfor (i in seq(1:8)){  print(physioData(paste0("POST_PQ",i)))}presenceQGrouped  <- presenceQ %>% group_by(Quad_Cat) %>% summarize_all(.funs = list(mean = mean))long <- presenceQGrouped %>%  pivot_longer(    cols = `POST_PQ1_mean`:`POST_PQ8_mean`,    names_to = "metric",    values_to = "value")longRaw <- presenceQ %>%  pivot_longer(    cols = `POST_PQ1`:`POST_PQ8`,    names_to = "metric",    values_to = "value")compareAllQuestions <- t_test(longRaw %>% group_by(Quad_Cat), value ~ metric)comareAllSubset <- compareAllQuestions %>% filter(p.adj.signif != "ns")long %>% select(-metric) %>%  group_by(Quad_Cat) %>% summarise(mean = mean(value))x <- long %>% select(-metric) %>% filter(Quad_Cat == 3)y <- long %>% select(-metric) %>% filter(Quad_Cat == 1)t.test(x = x, y = y, paired = FALSE, conf.level = 0.95)library(rstatix)t_test(longRaw, value ~ Quad_Cat)t_test(longRaw, value ~ Num_Code)# bartlett.test(test, value ~ Num_Code)ggplot(long) +  geom_bar(aes(x = metric, y = value, fill = factor(Quad_Cat)),           stat = "identity", position = position_dodge2()) +  scale_x_discrete(labels= c("PQ1", "PQ2", "PQ3", "PQ4", "PQ5", "PQ6", "PQ7","PQ8")) +  scale_y_continuous(breaks = seq(1,5,1))+  labs(y = "Average Score", x = "Presence Question")ggplot(long) +  geom_bar(aes(x = Quad_Cat, y = value, fill = metric),           stat = "identity") +  scale_x_discrete(labels= c("PQ1", "PQ2", "PQ3", "PQ4", "PQ5", "PQ6", "PQ7","PQ8"))# High fear 7 vs low fear 2x <- longRaw %>% select(-metric) %>% filter(Num_Code == 7) %>% pull(value)y <- longRaw %>% select(-metric) %>% filter(Num_Code == 4) %>% pull(value)t.test(x = x, y = y, paired = FALSE, conf.level = 0.95)var.test(x, y)presenceQData(7,4)
```