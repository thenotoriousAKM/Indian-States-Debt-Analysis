# Analysis of the Total Outstanding Liabilities of Indian States

This report investigates the growth of Total Outstanding Liabilities (TOL) in Indian states over the past decade and analyzes the potential demographic and geographic factors influencing this trend

## Data
### Total Outstanding Liabilities   
Source: *State Finances: A Study of Budgets.*

### Population, Projected Growth Rate, Area (km²) and Population Density
Source: *Census 2011 and [Indian Population Analysis](https://www.kaggle.com/datasets/themrityunjaypathak/2011-census-of-india)*  
License: [CC0](https://creativecommons.org/publicdomain/zero/1.0/)

## Limitations
* Reliance on 2011 Census Data
* Exclusion of state-specific policies or central funding effects
* Data Granularity
* Projections Based on 2011 Census Growth Rates 
* Literacy Rate taken from 2011 Census
* Included states that are only in the *State Finances: A Study of Budgets.* by the RBI

## Results
### Average Growth
| ![Average Growth Line Chart](<Visualizations/average growth rate line chart.png>) |
|:----------------------------------------:|
| *Fig. 1: Average Growth Line Chart*  |

| ![Average Growth Scatter Plot](<Visualizations/average growth rate scatter plot.png>) |
|:----------------------------------------:|
| *Fig. 2: Average Growth Scatter Plot*  |

2024 has the highest growth for the average debt, while 2023 sees the lowest growth.

| ![Statewise Debt Growth Trends](<Visualizations/lineplot statewise debt.png>) |
|:----------------------------------------:|
| *Fig. 3: Statewise Debt Growth Trends*  |

Yes, this graph might be difficult to interpret at first glance, but the following breakdown makes it easier:

#### States with Stable Debt Growth:
- Andhra Pradesh
- Bihar
- Odisha
- Karnataka
- Jharkhand
- Kerala  

###### Stable debt levels can indicate well-planned borrowing strategies.

#### States with High Growth Rates:
- Tamil Nadu
- Uttar Pradesh
- West Bengal
- Maharashtra
- Rajasthan  

###### High debt growth rates can suggest:
1. Poor borrowing strategies.
2. Borrowings for large-scale development projects.
3. States facing economic hardship.

#### States with Low or Negligible Debt Growth:
- Goa
- Mizoram
- Nagaland
- Tripura
- Sikkim  

###### Low growth rates can be attributed to lower populations, which means less expenditure.

#### States with Fluctuating Debt Growth:
- Himachal Pradesh
- Punjab
- Haryana  

###### Inconsistent growth rates could result from:
1. Irregular borrowing patterns.
2. Economic instability.

#### States with Very High Debt Levels:
- Tamil Nadu
- Uttar Pradesh
- Maharashtra
- West Bengal  

###### These states have some of the highest total debt levels and growth due to:
1. Heavy development projects.
2. Larger populations to cater to.

### Highest Debt Years for Each State
| ![Highest Debt Year for Each State](<Visualizations/which year state had highest debt.png>) |
|:----------------------------------------:|
| *Fig. 4: Highest Debt Year for Each State*  |

- 26 states peaked in 2024.
- 2 states peaked in 2020.
- 2 states peaked in 2017.

##### From which we can make out that debt has been growing for most states, since highest accumulated debt is from 2024.

### Highest Debt State for Each Year
| ![Highest Debt State for Each Year](<Visualizations/during a certain year what state had highest debt.png>) |
|:----------------------------------------:|
| *Fig. 5: Highest Debt State for Each Year*  |

- Uttar Pradesh had the highest debt for 6 years - 2016, 2017, 2018, 2019,2020, 2021 
- Tamil Nadu led for 3 years - 2022, 2023, 2024
- Maharashtra led for 1 year - 2015

##### Tamil Nadu has been the leading debtor in recent years, growing significantly since 2022.
- This is not suprising since Tamil Nadu has seen a lot of developments recently in terms of Social and Technological Infrastructure.

### Hypothetical Debt Per Person for 2024
| ![Debt Per Person for 2024](<Visualizations/debt per person for 2024.png>) |
|:----------------------------------------:|
| *Fig. 6: Debt Per Person for 2024*  |

##### A hypothetical measurement on how much of the State's Debt a single person carries, the objective being to give an idea or seriousness of the debt level.

States with smaller populations tend to have higher debt per person?
In this case: Goa and Sikkim

###### We will be checking this in the Analysis below.


### Does Debt and Population Have a Connection?
We examine both Pearson and Spearman correlations using heatmaps to determine the relationship between population and debt.

#### For 2024
| ![Correlation Heatmap (2024)](<Visualizations/corelation heatmap- debt_2024 and pop_2024.png>) |
|:----------------------------------------:|
| *Fig. 7: Correlation Between Debt and Population for 2024*  |

The heatmap indicates a positive correlation: States with larger populations accumulated more debt.

#### For 2015 to 2024
##### Pearson’s Correlation
| ![Pearson's Correlation](<Visualizations/pearsons corelation of L-all and P-all.png>) |
|:----------------------------------------:|
| *Fig. 8: Pearson's Correlation Between Debt and Population (2015–2024)*  |

##### Spearman’s Correlation
| ![Spearman's Correlation](<Visualizations/spearmans corelation of L-all and P-all.png>) |
|:----------------------------------------:|
| *Fig. 9: Spearman's Correlation Between Debt and Population (2015–2024)*  |

Both Pearson's (linear) and Spearman's (non-linear) correlations show a strong positive relationship between population and debt over the past 10 years (2015–2024).

#### Why?
##### States with larger populations likely require more resources and infrastructure, leading to higher expenditures.

### Does Debt and State Size Have a Connection?
We analyze the relationship between state size (km²) and debt.

| ![Spearman's Correlation: State Size and Debt](<Visualizations/spearman corelation between state size and debt.png>) |
|:----------------------------------------:|
| *Fig. 10: Spearman's Correlation Between State Size and Debt*  |

The correlation indicates that larger states tend to accumulate more debt.

#### Why?
Larger states may require more infrastructure, such as:
- Longer roads connecting districts.
- More public facilities.

#### Challenges:
1. **Area Alone Doesn’t Reflect Utilized Space.**  
2. **Debt Impacts People, Not Land.**  
3. **Population-Dense States Have Different Needs.**  

To address this, we analyze population density instead.

| ![Scatterplot: Population Density vs. Average Debt](<Visualizations/scatterplot population density vs average debt.png>) |
|:----------------------------------------:|
| *Fig. 11: Scatterplot - Density vs. Average Debt*  |

| ![Heatmap: Density vs. Debt (2024)](<Visualizations/heatmap density and avg_debt.png>) |
|:----------------------------------------:|
| *Fig. 12: Correlation Between Debt (2024) and Population Density*  |

##### Both Fig. 11 and Fig. 12 show weak correlations, confirming that population density does not significantly impact debt levels.


### Summary of Analysis: Population, Area, and Population Density vs. Debt
1. **Population:** Positive correlation—states with higher populations tend to have more debt.
2. **State Size:** Positive correlation—larger states tend to accumulate more debt.
3. **Population Density:** Weak correlation—density has minimal impact on debt levels.

## Literacy Rate
##### We have an accuracy concern for this part of the analysis since the literacy rates are ass of the 2011 Census and considering the recent advancements in the Indian Education Sector we feel like our values can be outdated.

 For an Idea of how the Literacy Rate is distributed we have plotted a bar graph:

| ![Visualizations/literacy rate barh chart.png](<Visualizations/literacy rate barh chart.png>) |
|:----------------------------------------:|
| *Fig. 13: Literacy Rate*  |

##### Above 90% Literacy:
1) Kerala
2) Mizoram

##### 80% Range
1) NCT Delhi
2) Puducherry
3) Tripura
4) Tamilnadu
5) Sikkim
6) Maharashtra
7) Himachal Pradesh
8) Goa

##### Remaining States fall below the 80% Treshold!

### Does Literacy Rate have any impact on the debt accmulation of a state?

| ![Visualizations/literacy vs debt scatterplot.png](<Visualizations/literacy vs debt scatterplot.png>) |
|:----------------------------------------:|
| *Fig. 14: Scatterplot: Literacy Rate vs Debt*  |

From this plot we can notice a negative correlation between the variables, but we dont want to jump into conclusions.

Let's try plotting more

| ![Visualizations/heatmap literacy rate and debt.png](<Visualizations/heatmap literacy rate and debt.png>) |
|:----------------------------------------:|
| *Fig. 15: Heatmap: Literacy Rate vs Debt*  |

##### Our plot gives us Negative Correlation which further confirms that Literacy Rate has no impact on debt accumulation

Before we get our assumptions on why?, we can plot:
Literacy Rate vs Average Debt

| ![Visualizations/heatmap avg_debt and literacy rate.png](<Visualizations/heatmap avg_debt and literacy rate.png>) |
|:----------------------------------------:|
| *Fig. 16: Heatmap: Literacy Debt vs Average Debt*  |

- -0.3 - Which is again negative correlation, similiar to the previous one.

#### Let's try to explain why?, Our Assumptions
* You cannot just cater to only the literate people, every person of a state regardless of their social,economic backgrounds needs to be valued.
* Even if there are many literate people, it does'nt mean that always the right decisions have to be taken.
* But, this literacy rate is from 2011, as of current day data our outcome might change!
  

## Conclusion
From this short Analysis we have got the following knowledge:
1) Debt Growth Trends:
We identified varying debt growth rates across states, providing an overview of how states manage their financial liabilities over time.

2) Population Impact:
There is a clear correlation between population size and state debt, highlighting the potential influence of population-driven demands on state expenditures.

3) Impact of State Area:
The total geographical area of a state shows a noticeable relationship with its debt levels, suggesting that larger states might face higher infrastructure and administrative costs.

4) Population Density:
Population density was found to have minimal impact on state debt, indicating that debt levels are not strongly influenced by how concentrated the population is within a state.

5) Literacy Rate:
The literacy rate appears to have no significant correlation with state debt, suggesting that educational attainment alone does not directly affect financial liabilities.


