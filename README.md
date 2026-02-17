# Game Analysis: Do Harder Levels Cause Player Churn?
## Data Overturned a Common Assumption
It is widely assumed that hard levels cause players to quit.

The data says otherwise.
  Hard levels do not cause universal churn.
  They disproportionately impact a small behavioral segment.

Community feedback amplifies frustration signals, this causal analysis reveals:

1. 14.6% of players show high difficulty sensitivity (ITE = 0.175)
2. 24.5% remain highly resilient (ITE = 0.118)
3. 60.9% disengage for reasons unrelated to struggle (ITE = 0.134)

The majority of players are resilient to higher difficulty levels.

## Analysis Workflow
Instead of relying on community signals, a rigorous analysis workflow is introduced:

1. Set up Causal Problem
1.1 Treatment, Outcome, Pre-treatments, Post-treatments and Confounders 
1.2 Identification Assumptions 

2. Overall Impact vs. User-Level Impact
2.1 IPW and Doubly Robust 
2.2 Overall ATE, ITE and HTE

3. Different Players, Different Reactions
3.1 Cluster players based on gameplay features

## Core idea
ATE, ITE, and HTE quantify the causal impact of hard levels on churn at different levels of granularity.
Causal assumptions remove bias.
Clustering reveals underlying structure.

Together, they transform noisy correlations into segment-level mechanisms and actionable product insight.

## Scalability
Decision Principle: Move from average optimization to segment-aware optimization.

This framework is scalable across both technical and product dimensions.
### Technical Extensions
ITE Estimation: Causal Forests, Meta-learners (S-/T-/X-learners)
Segmentation Methods: Gaussian Mixture Models (GMM), Hierarchical Clustering

### Product Applications
Business: Pricing strategies, Personalized recommendation systems, Coupon allocation and uplift modeling
Public Health: Medical treatment evaluation and Policy impact assessment

In each case, the key question shifts from:
“Does it work on average?” to “For whom does it work, and how should we act accordingly?”

## Data Information
The essential rule for data processing is 

data resource:






