# Game Analysis: Do Harder Levels Cause Player Churn?
## Data Overturned a Common Assumption

Community feedback can create the impression that hard levels are the primary reason players quit.

The data shows a different story:

> **Hard levels do not make everyone quit.**  
> **They mainly affect a small group of players.**

### What the Analysis Reveals

- **14.6%** of players are highly sensitive to difficulty *(HTE = 0.175)*  
- **24.5%** remain resilient even when levels are hard *(HTE = 0.118)*  
- **60.9%** lose interest for reasons not directly related to difficulty *(HTE = 0.134)*  

> **Most players can handle higher difficulty levels.**

## Analysis Workflow
Instead of relying on community signals, a rigorous analysis workflow is introduced:

**1. Set up Causal Problem**
- Treatment, Outcome, Pre-treatments, Post-treatments and Confounders 
- Identification Assumptions 

**2. Overall Impact vs. User-Level Impact**
- IPW and Doubly Robust 
- Overall ATE, ITE and HTE

**3. Different Players, Different Reactions**
- Cluster players based on gameplay features

<img width="1714" height="425" alt="OverviewFigure" src="https://github.com/user-attachments/assets/b49c8e1f-9fd5-4f75-b218-c3d6055fbe4a" />

### Project Structure
- Dataset_Preparation.ipynb  
  Data cleaning, preprocessing, and variable validation.

- GameAnalysis_main.ipynb  
  Causal estimation (ATE, ITE, HTE) and clustering analysis.

- dataset.csv  
  Raw game behavior dataset.

- game_data.csv  
  Output by Dataset_Preparation.ipynb and applied in GameAnalysis_main.ipynb.

## Core idea
ATE, ITE, and HTE quantify the causal impact of hard levels on churn at different levels of granularity.
Causal assumptions remove bias.
Clustering reveals underlying structure.

Together, they transform noisy correlations into segment-level mechanisms and actionable product insight.

## Scalability
Decision Principle: Move from average optimization to segment-aware optimization.
This framework is scalable across both technical and product dimensions.

### Technical Extensions
- ITE Estimation: Causal Forests, Meta-learners (S-/T-/X-learners)
- Segmentation Methods: Hierarchical Clustering

### Product Applications
- Business: Personalized recommendation systems, Coupon allocation
- Public Health: Medical treatment evaluation and Policy impact assessment

In each case, the key question shifts from:
“Does it work on average?” to “For whom does it work, and how should we act accordingly?”

## Data Information
There are two key aspects for data cleaning and reconstruction: Operational Accessibility and Meaning Consideration.

Operational accessibility involves standardizing column names, removing redundant variables (e.g., duplicates or non-unique columns), and handling missing values when necessary. These steps ensure that the data is properly structured and fully usable for subsequent analysis.

Meaning consideration focuses on validating the conceptual relevance of each variable within the concrete scenario. In this case, churn and hard-level variables are constructed by transforming continuous measures into binary indicators based on data-driven distribution thresholds. These two variables are essential for analyzing the topics of "churn rate" and "hard level."

Distribution checks are conducted for each variable to assess domain coverage and statistical validity. Variables with no variance provide no analytical value and are removed. For highly imbalanced data, additional evaluation metrics such as F1-score are used instead of relying solely on accuracy.

### Data resource: 
The initial raw data was collected from various gaming platforms, capturing key player metrics and behaviors. https://github.com/pancham8675/player_churn_prediction/blob/main/datasets/final_dataset.csv







