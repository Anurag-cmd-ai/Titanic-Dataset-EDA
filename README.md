# Titanic Dataset - Exploratory Data Analysis (EDA)

Built an end-to-end Exploratory Data Analysis (EDA) on the classic Titanic dataset using Python, Pandas, NumPy, Matplotlib, and Seaborn. Cleaned and prepared data by handling missing values (mean age imputation and cabin placeholder mapping) and uncovered key demographic insights—revealing that 38.4% of passengers survived, young adults aged 20–30 formed the largest age group, and women (particularly in first class) had significantly higher survival rates.

## Objective
Understanding the passenger demographics and ticket features is a crucial first step before building any predictive models for the Titanic dataset. This project focuses strictly on data wrangling and visualization, transforming raw data into actionable insights.

## Tech Stack
This analysis was conducted using Python and the following data science libraries:
*   **`pandas`**: For data ingestion, manipulation, and cleaning.
*   **`numpy`**: For numerical and array operations.
*   **`matplotlib.pyplot`**: For structuring and plotting static visualizations.
*   **`seaborn`**: For creating statistical, aesthetically pleasing plots (e.g., KDEs, count plots).

## Data Inspection & Cleaning
Proper data types and complete data are essential for accurate analysis. The following cleaning steps were applied:
1.  **Missing Age Values:** The `Age` column was missing ~19.8% of its data (177 null values). Since the age distribution closely followed a normal distribution (skewness ~0.38), the missing values were imputed using the overall mean age. The column was then converted to an integer datatype.
2.  **Missing Cabin Data:** Null values in the `Cabin` column were filled with a placeholder string `'M'` (Missing).

## Key Insights & Visualizations
Through univariate analysis, several key observations were made regarding the passengers:

*   **Age Distribution:** Histograms and KDE plots indicate that the majority of passengers were between 20 and 30 years old. Boxplots confirmed that while there were elderly passengers (up to 80 years old), these were valid entries rather than outliers.
*   **Fare Distribution:** The fare prices are highly right-skewed (positive skewness of ~4.78). Approximately 50% of the passengers paid less than $14, while the majority paid between $0 and $25. High fares (e.g., >$250) exist but represent valid grouped ticket purchases for families rather than data errors.
*   **Survival Rate:** A pie chart and count plot visualization revealed that only 38.4% of the passengers in this dataset survived the disaster.
*   **Survival Rate v/s Gender:** The visualization revealed that among the passengers survived most were women especially from PClass 1.
*   **Gender:** A standard count plot was generated to observe the overall distribution of male and female passengers onboard.
  

##  Feature Engineering
To better understand passenger groupings, a new feature was created:
*   **FamilySize:** By visualizing and merging the `SibSp` (siblings/spouses) and `Parch` (parents/children) columns, a unified `FamilySize` feature was generated (`SibSp` + `Parch` + 1).
*   **FamilyType:** This new metric provides a clearer picture of whether a passenger was traveling alone or with a large family.Also it gave info that passenger with a medium size family had the highest survival rate.
*   **Deck:** Classifying people surivival rate .People belonging to Deck B,C,D,E,F had the highest survival rate.


##  Author
Anurag Tiwari
