# Startup Health Scoring Model - README

## Project Overview

This project implements a comprehensive scoring system to evaluate startup health and potential, similar to a credit score but tailored for startups. The model analyzes key business indicators to generate a composite score (0-100) for each startup in the dataset.

## Features

- **Data Preprocessing**: Normalizes all numeric features to a 0-1 scale
- **Custom Scoring Formula**: Weighted evaluation across multiple dimensions
- **Comprehensive Analysis**: 
  - Ranks all startups by health score
  - Identifies top and bottom performers
  - Provides detailed explanations for scores
- **Visualizations**: 
  - Score distribution charts
  - Correlation heatmaps
  - Comparative analysis plots

## Dataset Structure

The dataset contains 100 fictional startups with the following features:

| Column Name               | Description                                      |
|---------------------------|--------------------------------------------------|
| startup_id                | Unique ID of the startup                        |
| team_experience           | Average years of relevant experience (1-10)     |
| market_size_million_usd   | Total addressable market (TAM) in million USD   |
| monthly_active_users      | Current number of monthly active users          |
| monthly_burn_rate_inr     | Average monthly expenses (INR)                  |
| funds_raised_inr          | Total funding raised so far (INR)               |
| valuation_inr             | Current company valuation (INR)                 |

## Methodology

1. **Data Normalization**:
   - Min-Max scaling (0-1 range)
   - Direction-aware normalization (higher values can be better or worse)

2. **Scoring Model**:
   - Weighted combination of factors:
     - Team Experience (15%)
     - Market Size (20%)
     - Monthly Active Users (25%)
     - Burn Rate (10%)
     - Funds Raised (15%)
     - Valuation (15%)

3. **Analysis**:
   - Composite scores calculated (0-100 scale)
   - Startups ranked by score
   - Statistical analysis of score distribution

## How to Use

1. **Requirements**:
   - Python 3.7+
   - Required packages: pandas, numpy, matplotlib, seaborn, scikit-learn

2. **Running the Analysis**:
   ```bash
   python startup_scoring.py
   ```

3. **Outputs**:
   - Console output with top/bottom performers and score statistics
   - Visualizations showing score distributions and correlations
   - CSV file (`startup_scores_ranked.csv`) with all startups and their scores

## Key Findings

The analysis reveals:
- The distribution of startup health scores across the dataset
- Which factors contribute most to high scores (strong correlations)
- Characteristics of top-performing vs. underperforming startups
- The relationship between valuation and composite score

## Customization

The model can be adapted by:
1. Adjusting the weights in the scoring formula
2. Changing normalization directions for specific features
3. Adding or removing evaluation criteria

## Example Interpretation

A top-performing startup typically shows:
- Strong team experience (8-10/10)
- Large market size ($500M+)
- High user engagement (50,000+ MAU)
- Sustainable burn rate
- Significant funding and valuation

## License

This project is open-source and available for use under the MIT License.

## Contact

For questions or suggestions, please open an issue in the project repository.
