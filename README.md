# Tampa Bay Lightning Performance Analysis: Model Interpretability Project

## Project Overview
This data science project analyzes the Tampa Bay Lightning's performance to identify which player performance metrics most significantly contribute to team success. The analysis aims to inform decisions on player development, lineup optimization, and talent acquisition, which is particularly valuable for a team like the Lightning who need to maintain high performance while managing salary cap constraints.

## Business Problem
For Tampa Bay Lightning management, understanding which player performance metrics most significantly contribute to team wins is essential for:
- Strategic player development
- Optimal lineup configurations
- More effective talent acquisition
- Managing salary cap constraints while maintaining competitive performance

## Data
The analysis uses two primary datasets:
- `TBL_Player.csv`: Player-level performance metrics (6,390 rows, 156 columns)
- `TBL_Team.csv`: Team-level performance data (355 rows, 109 columns)

The datasets contain various performance metrics including:
- Player game scores
- Ice time
- Expected goals (xG)
- Corsi and Fenwick percentages
- High-danger scoring chances
- Shots on goal statistics

## Methodology
1. **Exploratory Data Analysis (EDA)** to understand team and player performance metrics
2. **Player Performance Analysis** to identify key contributors
3. **Feature Aggregation** of individual player data to game level
4. **Model Building** using Random Forest to predict game outcomes
5. **Feature Importance Analysis** to identify critical performance factors
6. **Player Chemistry Analysis** to understand teammate impacts
7. **Undervalued/Overvalued Player Identification** based on traditional vs. impact metrics
8. **Defensive Effectiveness Analysis** to identify top defensive players
9. **Loss Pattern Identification** to suggest tactical adjustments

## Key Findings

### Team Performance
- The Lightning had a record of 39-32 (54.9% win percentage)
- **Home vs. Away performance disparity**: 68.6% win rate at home versus 41.7% on the road
- Top performance factors in wins:
  - Higher high-danger shots for (+26.3% compared to losses)
  - Better expected goals percentage (+23.4%)
  - More takeaways (+17.0%)
  - Fewer high-danger shots against (-28.4%)

### Player Impact
- **Nikita Kucherov** has the highest game score (1.47) and points (101)
- **Top 5 players by average Game Score**:
  1. Nikita Kucherov (1.47)
  2. Brandon Hagel (1.19)
  3. Jake Guentzel (1.01)
  4. Brayden Point (0.97)
  5. Anthony Cirelli (0.93)

- **Kucherov-specific impact model** achieved 93% accuracy in predicting team wins, with key factors being:
  - Ice time (26.5% importance)
  - On-ice expected goals percentage (24.6%)
  - Game score (15.0%)

- The Lightning win 76.3% of games when Kucherov's game score is above 1.32, but only 27.6% when below this threshold

### Undervalued/Overvalued Players
- **Potentially undervalued players**:
  - Michael Eyssimont (C)
  - Gage Goncalves (C)
  - Emil Lilleberg (D)
  - Darren Raddysh (D)

- **Potentially overvalued players**:
  - Brandon Hagel (L)
  - Victor Hedman (D)
  - Nikita Kucherov (R) - highly valuable but extremely high usage

### Defensive Specialists
- **Top defensive forwards** (lowest xG against per 60):
  - Michael Eyssimont
  - Nikita Kucherov
  - Gage Goncalves

- **Top defensive defensemen**:
  - Darren Raddysh
  - Nick Perbix
  - Emil Lilleberg

### Opponent-Specific Challenges
- **Toronto**: 0% win rate despite decent expected goals metrics
- **Florida**: 33.3% win rate with significantly higher high-danger shots against
- **Philadelphia**: 33.3% win rate despite favorable possession metrics

## Recommendations

1. **Lineup Optimization** (Estimated +5 points)
   - Prioritize the Kucherov-Guentzel pairing
   - Ensure optimal deployment of top 5 players by Game Score

2. **Increase Roles for Undervalued Players** (Estimated +4 points)
   - Give more responsibility to Michael Eyssimont, Gage Goncalves, Emil Lilleberg, and Darren Raddysh
   - Reduce reliance on potentially overvalued players

3. **Develop Specific Road Game Strategies** (Estimated +7 points)
   - Address the significant home/away performance gap
   - Implement more conservative approach to counteract road disadvantages

4. **Focus on Limiting High-Danger Chances** (Estimated +3 points)
   - High-danger shots against show the largest negative correlation with winning
   - Implement tactical adjustments to reduce these opportunities

5. **Implement Opponent-Specific Game Plans** (Estimated +3 points)
   - Develop tailored approaches for Toronto, Florida, and other challenging opponents
   - Focus on tactical adjustments for close games

## Technologies Used
- Python
- Pandas & NumPy for data manipulation
- Scikit-learn for machine learning models
- Matplotlib & Seaborn for data visualization
- Jupyter Notebook for analysis environment

## Future Work
- Incorporate additional seasons of data for trend analysis
- Perform network analysis to further explore player chemistry
- Develop position-specific performance models
- Analyze penalty kill and power play effectiveness separately
- Create deployment optimization tools for coaching staff
