# Bike Purchase Data Analysis Project (MS Excel)

# **Introduction**

This project analyzes a bike purchase dataset to extract insights that will help a bike seller make informed marketing decisions and ultimately improve sales.

# **Purpose of the Project**

The primary objectives of this analysis are:

Identify key demographics that purchase bikes more frequently. This will help the seller focus marketing efforts on the most promising customer segments to maximize sales.

Recognize underexplored demographics that have the potential to purchase bikes at a higher rate. This will guide the seller in redirecting marketing strategies from less interested groups to those with higher potential for conversion.

# **Dataset Overview**
The dataset is obtained from the open-source platform 'Kaggle' and is accessible to the general public for use.

The dataset contains 106 identifiers and 12 variables. The variables are: Marital status, Gender, Income, Children, Education, Occupation, Homeowner, Cars, Commute, Region, Age, and Purchased bike.

Note: Variables, in this case, are the attributes of identifiers that may have influenced their decision of whether or not to purchase a bike.

# **Dataset Cleaning**
The first step in data analysis is often data cleaning. In this case, the dataset was cleaned after a data overview.

The dataset was copied and pasted into a new Excel sheet named 'Working Sheet.' Data cleaning and transformation were conducted on this sheet while retaining the raw data in its original form on the original Excel sheet.

The first step in data cleaning was removing any duplicates from the dataset.
Method: Select the whole dataset (Ctrl+A) > Data > Remove Duplicates > Data has headers.

In the dataset, 26 duplicates existed (and were eliminated), leaving 1,000 unique values. Each column was checked for any inconsistencies or inaccuracies. Since no column contained any inconsistency or inaccuracy, the dataset was transformed.

# **Dataset Transformation**

Each column was reviewed for necessary transformations in data type, values, or format.

In the 'Marital status' column, 'M' data values were replaced with 'Married,' and 'S' data values were replaced with 'Single' for clarity.
Process: Select column and use the Find and Replace function available in the Home tab.

In the 'Gender' column, 'M' data values were replaced with 'Male,' and 'F' data values were replaced with 'Female' for better understanding.

The 'Income' column was converted to currency format.
Process: Select column > Number > Currency. Additionally, values were rounded to whole numbers.

In the 'Commute' column, '10+ miles' data values were replaced with 'More than 10 miles' using the Find and Replace function. This transformation enabled efficient sorting, as Excel recognized 'More than 10 miles' as the greatest value in the column.

Since the 'Age' column contained many distinct values, a new column named 'Age Bracket' was created to simplify visualization.
Process: Insert column (right of 'Age' column).

Distinct age values were grouped into ranges:

'Senior' (Age ≥ 60)

'Middle Age' (Age ≥ 41)

'Adult' (Age ≥ 25)

The IFS function was used to categorize ages:

=IFS([@Age]>=60, "Senior", [@Age]>=41, "Middle Age", [@Age]>=25, "Adult")

The formula was applied to the entire 'Age Bracket' column, making visualization easier.

Since the remaining columns did not require any transformation, the clean and transformed dataset was analyzed.

# **Dataset Analysis**

A new worksheet, 'Pivot Tables,' was created. All analysis was performed on this sheet. Data from the 'Working Sheet' was copied and pasted onto this new sheet.

The analysis focused on answering the following questions:

Does the level of income influence the decision to purchase a bike?

Does commute distance affect bike purchases?

Which age group is more interested in buying bikes?

First Analysis

A Pivot Table was created to compare the average income of males versus females who did or did not purchase a bike.
Process: Insert Pivot Table > Select dataset from 'Working Sheet' > Rows: Gender > Columns: Purchased bike > Values: Average of Income.

Findings:

Bikes were purchased more by individuals with higher average income compared to non-purchasers.

The average income of male identifiers was higher compared to female identifiers.

Even among non-purchasers, male identifiers had higher average income than female purchasers.

Second Analysis

A Pivot Table was created to compare commute distance with bike purchase decisions.
Process: Insert Pivot Table > Select dataset from 'Working Sheet' > Rows: Commute distance > Columns: Purchased bike > Values: Count of Purchased bike. Sort commute distance in ascending order.

Findings:

The largest target market based on commute distance was the '0-1 miles' category, which contained the highest number of identifiers.

As commute distance increased, the size of the target market decreased.

As commute distance increased, the number of bike purchases decreased.

Third Analysis

A Pivot Table was created to compare age brackets with bike purchases.
Process: Insert Pivot Table > Select dataset from 'Working Sheet' > Rows: Age Brackets > Columns: Purchased bike > Values: Count of Purchased bike.

Findings:

The largest target market based on age bracket was 'Middle Age' (41-59 years), which contained the highest number of identifiers.

The 'Middle Age' group had significantly higher bike purchases compared to the 'Senior' (60+ years) and 'Adult' (25-40 years) groups.

# **Recommendations to Bike Seller**

Based on the analysis, the following data-driven marketing strategies are recommended:

Target high-income individuals since they are more likely to purchase bikes.

Prioritize marketing to women within the same income bracket, as they show a higher purchase tendency than men at equivalent income levels.

Focus on individuals with a short commute (0-5 miles), especially 0-1 miles, as they represent the largest market.

Emphasize middle-aged buyers (41-59 years), as they are the most likely to purchase bikes.

By implementing these strategies, the bike seller can maximize marketing effectiveness and increase sales.

# **Conclusion**

The bike purchase analysis provides key insights that can guide the seller in optimizing marketing efforts. Findings suggest that high-income individuals, those with shorter commutes, and middle-aged buyers are the most likely to purchase bikes. By focusing on these demographics, the seller can develop more effective marketing strategies and improve sales.
