# NBA Performance, Usage, Salary and Retention Analysis

## Objective

This project investigates whether there is an **observational association** between player performance, on-court usage, salary, and **observed non-retention** in the same team in the following NBA season.

The analysis is conducted at the **player-season level**, using statistical association measures and probability concepts.

---

## Research Question

Is there an observational association between **low performance**, **low usage**, and **observed non-retention** in the same team in the following season?

---

## Dataset

The dataset used is:

`nba_stats_preprocessed.csv`

Each row represents a **player-season**.

### Main Variables

- `points`
- `total_minutes`
- `games_played`
- `salary_usd`
- `player_id`
- `team_abbreviation`
- `season`

---

## Methodology

### 1. Data Preparation

- Creation of a `player_season` identifier
- Construction of the variable:

**S = observed non-retention**

A player is considered **not retained** if they do not appear in the same team in the following season.

- Removal of last-season cases (no observable next season)

---

### 2. Quantitative Association

The following statistical measures are used:

- Covariance  
- Pearson correlation  
- Correlation matrix / heatmap  
- Scatter plot analysis  

Applied to:

- Points  
- Total minutes played  
- Games played  
- Salary  

> Correlation indicates **association**, not causality.

---

### 3. Discrete Random Variable

A discrete random variable is defined as:

**X = number of "low indicators" in a player-season**

#### Indicators:

- Points in the bottom quartile  
- Minutes played in the bottom quartile  
- Games played in the bottom quartile  

Thus:
X ∈ {0, 1, 2, 3}

Event:
B = (X ≥ 2)


Where **B represents low performance or low usage**.

#### Calculations:

- PMF (Probability Mass Function)  
- CDF (Cumulative Distribution Function)  
- Mean  
- Standard deviation  

---

### 4. Conditional Probability

The analysis compares:

- P(S | B)  
- P(S | not B)  

Difference:
P(S | B) - P(S | not B)


---

## Key Objective

To evaluate whether **observed non-retention** is more frequent among player-seasons classified as:

- low performance  
- low usage  

---

## Technologies Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Google Colab  

---

## Authors

- Vinícius Freitas — @vinifrts  
- João Pedro Muniz — @joaopedroms200-droid  

---

## Disclaimer

This analysis is **observational** and does not imply causality.

Observed non-retention does not indicate reasons such as trade, release, retirement, or contract decisions.
