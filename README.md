# eurovision-statistical-learning
Statistical analysis of Eurovision Song Contest success factors using logistic regression, decision trees, PCA, and K-means clustering in R. Achieved 79.6% prediction accuracy for top-10 placement.

# Eurovision Statistical Learning Analysis

## Project Overview

Comprehensive statistical analysis of Eurovision Song Contest data to identify factors influencing song success. Applied multiple statistical learning methods including logistic regression, decision trees, principal component analysis, and clustering to predict top-10 placement and analyze voting patterns.

## Key Findings

### Classification Models Performance

**Logistic Regression:**
- Accuracy: 73.8%
- Sensitivity: 71.0%
- Specificity: 76.6%
- Key predictors: BPM, style, gender, language

**Decision Tree:**
- Accuracy: 79.6% 
- Sensitivity: 76.1%
- Specificity: 83.0%
- Most important variable: **BPM** (93% importance)
- Better performance than logistic regression in capturing non-linear patterns

### Voting Pattern Analysis

**Principal Component Analysis:**
- PC1 explains 74.8% of variance
- PC2 explains 25.2% of variance
- Total variance explained: 100%

**K-Means Clustering:**
- Optimal clusters: 3 (via elbow method)
- Distinct voting behavior patterns identified
- Jury vs. Televote correlation: ρ=0.52 (p<0.001)

### Running Order Impact

**Linear Regression Results:**
- **Televote points:** Significant effect (p<0.001), R²=0.044
- **Jury points:** No significant effect (p=0.125), R²=0.007
- Maximum televote points awarded at position 12
- Maximum jury points awarded at position 11

### Success Factors

**Top 10 Placement Drivers:**
1. **BPM (Tempo):** Strongest predictor (93% variable importance)
2. **Style:** Opera shows highest churn rate (42.7%)
3. **Gender:** Male and female artists perform similarly
4. **Language:** English slightly favored

## Tools & Technologies

- **R:** Primary analysis environment
- **Statistical Methods:**
  - Logistic Regression
  - Decision Trees (CART)
  - Principal Component Analysis (PCA)
  - K-Means Clustering
  - Multiple Linear Regression
  - ANOVA
- **Visualization:** ggplot2, base R graphics

## Project Structure
├── presentation.pdf      # Complete analysis presentation
└── README.md            # Project documentation

## Analysis Workflow

### 1. Exploratory Data Analysis
- 565 observations, 44 variables
- Genre distribution (Pop: 48%, Ballad: 26%, Rock: 9%)
- Language analysis (58% English, 42% other languages)
- Gender distribution (Female: 47%, Male: 42%, Mix: 11%)

### 2. Classification Analysis
**Research Question:** What factors predict top-10 placement?

- Built two classification models: Logistic Regression and Decision Tree
- Decision tree outperformed logistic regression
- BPM emerged as the dominant predictor

### 3. Voting Patterns Analysis
**Research Question:** What factors explain jury vs. public voting differences?

- Applied PCA to reduce dimensionality
- K-means clustering revealed 3 distinct voting communities
- Correlation analysis showed moderate agreement between jury and public

### 4. Running Order Analysis
**Research Question:** Does performance order affect final scores?

- Linear regression analysis
- Found significant impact on televote (later positions favored)
- No significant impact on jury votes

## Academic Context

Completed as **Statistical Learning Project** at Università Cattolica del Sacro Cuore, Milan.

Dataset: Eurovision Song Contest data (2009-2023)

## Model Comparison

| Model | Accuracy | Sensitivity | Specificity | Best Use Case |
|-------|----------|-------------|-------------|---------------|
| Logistic Regression | 73.8% | 71.0% | 76.6% | Interpretability |
| Decision Tree | **79.6%** | **76.1%** | **83.0%** | **Prediction accuracy** |

## Key Insights

1. **Tempo matters:** BPM is the strongest predictor of success
2. **Jury vs. Public diverge:** Different factors influence professional vs. public votes
3. **Running order bias exists:** Later televote positions show advantage
4. **Style diversity:** Pop dominates but all genres can succeed
5. **Language impact minimal:** English slightly favored but not decisive

---

*Dataset: Eurovision Song Contest data (2009-2023) from Kaggle*
