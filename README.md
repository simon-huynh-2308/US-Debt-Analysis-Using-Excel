# US Debt Tracker Project

### Scenario: 
#### You were hired by a small debt agency in Washing DC that specializes in analyzing and forecasting public and private market debt. The US Government has requested an analysis of their public and governmental debt to answer some specific questions.

### Data Dictionary:
#### Debt Held by the Public: The portion of the US public debt that is held by individuals, corporations, foreign government
#### Intragovernmental Holdings: The portion of US public debt that is held by other US government agencies
#### Total Public Debt Outstanding: The sum of the debt held by the public and intragovernmental holdings.

### Questions:

#### 1. What was the Yearly Debt Percentage Increase for each year compared to the previous year?
#### 2. Which month historically have see the highest/ lowest increase in Total Debt?
#### 3. What is the projected growth of the publicly held debt in the next few years?

### Data Cleaning Process:

#### Purpose: The goal of cleaning data is because of the current raw dataset is not ideal for using Pivot Table with more than 7000 columns.

#### Process:
##### - Perform Transpose to flip the rows and columns. The dataset now is adjusted from vertical headings to horizontal headings.
##### - Format the cells to enhance visibility
##### - Apply Filter into the dataset
##### - Delete the blank rows
##### - Perform Ctr+H to replace Null values with Nothing 
##### - Adjust the values from Scientific Notation to Number 

### Questions 1:

#### For the purpose of this question, the last day of each year will selected to calculate the yearly debt percentage change. However, there are only 2 months in 2023, so the last day in Februry will be selected. The period year selected in this question will be 8 years (2015-2023).

#### The final day is the final amount of debt for both public, intragovernmental holding, and total public debt outstanding for each year. These values will be used to calculate the yearly debt percentage change for each year compared to the previous year.

#### The calculation is performed by subtracting the values of the current year from the previous year's values, then dividing the result by the previous year's values to determine the percentage change of Debt Held by the Public, Intragovernmental Holdings and Total Public Debt Outstanding.

#### Visualization: A Line Chart 

#### Insights:
##### - For the Total Public Debt Outstanding, in 2016 - 2019, the average increase was around 5%
##### - In 2020, there is a large spike that is most likely caused by the pandemic responses in the US

_________________________________________________________________________________________________
### Question 2:

#### Aggregate the data based on months
#### Use MONTH() function to extract month from Record Date
#### Create a Pivot Table with Record Date in Rows section, keeping only the Month, and Total Public Debt Outstanding in Values section, selecting Average
#### Visualization: A Bar Pivot Chart

#### Insights:
##### - Highest Debt Increase months historically occur during the months of January, February, November and December
##### - Lowest Debt Increase months historically occur during the months of April, May, June, and July
##### - During high months, there is an assumption that holidays in the US such as Thanksgiving and Christmas that people are more likely to spend money buying gifts for others. People might take debt for these months to buy these gifts.
##### - During low months, there are no major holidays. Therefore, people are taking on less debt during this time

_________________________________________________________________________________________________
### Question 3:

#### Create a Pivot Table with Record Data in Rows section, keeping only the Year, and Debt Held by the Public in Values section, selecting Max
#### Remove Years with null value
#### Apply FORECAST.ETS() function to predict Debt Held by the Public in 2023 till 2027
#### Visualization: Stacked Area Chart

#### Insights:
##### - From 1997 to 2007, there is an increase about 1 Trillion in Publicly Held Debt
##### - From 2008 to 2019, debt increased from 6 Trillion to 17 Trillion
##### - From 2020 to 2022, debt increased from 21.5 Trillion to 25 Trillion
##### - From 2023 to 2027, it is projected that Publicly Held Debt will increase to 33 Trillion
##### - Publicly Held Debt is projected to increase at a steady increased rate over the 5 years
##### - Options to further research would be Stock Market, Housing Market, Credit Card Purchases, and Unemployment Rates










