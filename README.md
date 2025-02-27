# EDA_Layoffs
## Introduction
This repository contains MySQL scripts used for exploratory data analysis (EDA) on layoffs dataset. The goal of this analysis is to understand trends, patterns, and key insights into layoffs across various companies, industries, and time periods.

## Objectives
- Identify companies with the largest layoffs.
- Analyze the percentage of workforce affected by layoffs.
- Detect patterns in layoffs based on funding levels.
- Explore industries and time periods with the highest layoffs.
- Uncover any outliers or significant trends in the data.

## Approach
The analysis is performed using MySQL queries executed on a staging table `layoffs_staging2`. The key steps include:
1. **Initial Data Exploration**: Retrieve the full dataset to understand its structure.
2. **Identifying Maximum Layoffs**: Find companies with the highest layoffs. 
3. **Analyzing Percentage of Workforce Laid Off**: Examine the range (min/max) of workforce reductions.
4. **Companies That Fully Laid Off Staff**: Identify companies where all employees were laid off.
5. **Impact of Funding on Layoffs**: Check if companies with higher funding faced significant layoffs.
6. **Largest Layoffs in a Single Event**: Identify which companies experienced the most severe layoffs in a single occurrence.

## Key Insights
- Some companies laid off 100% of their workforce, mainly startups that went out of business.
- Companies with high funding levels also faced large layoffs, suggesting financial backing didn't always prevent layoffs.
- Industries such as **tech startups** and **fintech** were heavily impacted.
- Certain periods saw significant spikes in layoffs, potentially correlating with economic downturns.
- Outliers in the dataset indicate extraordinary layoffs that require further investigation.


## Conclusion
This analysis provides a foundational understanding of layoffs trends and their implications.
---

```sql
-- Example Query: Companies with the largest layoffs
SELECT * FROM layoffs_staging2 ORDER BY total_laid_off DESC LIMIT 10;
```
