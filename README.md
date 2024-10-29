
# Analyzing Customer Churn in Power BI
- **Churn Rate** : The churn rate, also known as the rate of attrition or customer churn, is the rate at which customers stop doing business with an entity. There are multiple ways to calculate churn and it varies across the industries.
- **Simplified Formula**: Churn Rate = Customers Lost / Total Number of Customers 
- **Attrition**: It typically refers to the gradual reduction in the number of people, employees, or customers over time. In a business context, it often describes the rate at which employees leave a company or customers stop engaging with a business.
## Overview :

In this project, we will analyze a fictional dataset from a telecom provider, Databel, to uncover insights into the drivers of customer churn. By examining patterns within the data, we aim to identify key factors that influence customer retention and help inform targeted interventions.

**Project Workflow:**
- **Data Quality Assessment:** Perform initial checks to ensure data completeness, accuracy, and consistency.
- **Exploratory Data Analysis (EDA):** Conduct in-depth exploration to understand data distributions, relationships, and potential outliers.
- **Data Analysis and Visualization:** Apply analytical methods and visualizations to identify trends, correlations, and churn indicators.
- **Dashboard Creation:** Develop an interactive dashboard to present insights and enable stakeholders to explore key findings in real time.




## Link to Dataset

 - [DataBel Telecom Dataset](https://github.com/PriyaSree13/DataBel-Customer-Churn-/blob/main/Databel%20-%20Data.csv)

- [Power BI File](https://app.powerbi.com/groups/me/reports/f3615d38-4d23-45b3-8bbb-9bc174257104/ReportSectionb8a95ff9779ce50e0c04?experience=power-bi)



## Metadata

### Customer Status:

| Parameter       | Type     | Description                                                        |
| :-------------- | :------- | :----------------------------------------------------------------- |
| `Customer ID`   | `string` | The unique ID that identifies a customer                           |
| `Churn Label`   | `string` | Contains "Yes" or "No" to indicate if a customer churned           |
| `Churn Reason`  | `string` | The particular reason why the customer ended the contract          |
| `Churn Category`| `string` | Groups multiple churn reasons together for analysis purposes       |


### Demographics:

| Parameter        | Type     | Description                                                                                  |
| :--------------- | :------- | :------------------------------------------------------------------------------------------- |
| `Under 30`       | `string` | Indicates if the customer is under 30 with "Yes" or "No"                                     |
| `Senior`         | `string` | Indicates if the customer is 65 or above with "Yes" or "No"                                  |
| `Age`            | `integer`| The age of the customer                                                                      |
| `Gender`         | `string` | The gender of the customer, indicated by "Male", "Female", or "Prefer not to say"            |


### Contract Information: 

| Parameter                 | Type     | Description                                                                                              |
| :------------------------ | :------- | :------------------------------------------------------------------------------------------------------- |
| `Contract Type`           | `string` | Contains “Month to Month”, “One Year” or “Two Year”                                                      |
| `Payment Method`          | `string` | Preferred payment method of the customer indicated with “Credit Card”, “Direct Debit” or “Paper Check  |
| `State`                   | `string` | The code of the state where the customer lives  
| `Phone Number`            | `string` | Phone number of the customer                                                                             |
| `Group`                   | `string` | The group name or identifier                                                                             |
| `Number of customers in a group` | `integer` | The number of customers in a group|

### Subscription Types & Charges:

| Field Name                      | Description                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| `Account Length (in months)`  | The number of months the customer has been with the service                                                   |
| `Local Calls`               | Amount of local (within the US) calls from the customer                                                        |
| `Intl Calls`                 | Amount of international (outside the US) calls from the customer                                              |
| `Intl Mins`                  | The number of minutes spent calling internationally                                                            |
| `Intl Active`                | Indicates if the customer called internationally (Yes/No)                                                     |
| `Intl Plan`                   | Indicates if the customer has a premium plan to call internationally for free (Yes/No). This premium is reflected in the amount of the monthly charge |
| `Extra International Charges` | Contains the extra charges for international calls for customers who are not on an international plan         |
| `Customer Service Calls`     | The number of calls made to customer service                                                                  |
| `Avg Monthly GB Download`    | Contains the average monthly download volume in gigabytes                                                     |
| `Unlimited Data Plan`        | Indicates if the customer has free unlimited download capacity (Yes/No). This premium is reflected in the amount of the monthly charge |
| `Extra Data Charges`          | Contains the extra charges for data downloads for customers who are not on an unlimited plan                  |
| `Monthly Charges`            | Average of all monthly charges to the customer                                                                |
| `Total Charges`              | Sum of all monthly charges                                                                                   |





## Steps Followed :

### *Data Check:*

**Step 1) Data Loading**: Loaded the dataset from a text/CSV file into Power BI Desktop.

**Step 2) Measure Creation**: Created two measures to assess the customer count:
   - **Total Customers**: Using the `COUNT` function to tally the total customers.
   - **Unique Customers**: Using the `DISTINCTCOUNT` function to count unique customers.

**Step 3) Validation**: Confirmed that the count of unique customers matched the total count of customers, resulting in a total of 6,687.

<img width="438" alt="image" src="https://github.com/user-attachments/assets/7ac5847f-1441-4e3c-868a-b33bf206717d">


### *EDA (Exploratory Data Analysis):* 

**Step 4)** Created a new column named `Churned` using the following formula 
```DAX Churned = IF('dataset'[Churn Label] = "Yes", 1, 0)```

**Step 5)** Created a new measure to calculate the **Customer Churn Rate** using the churn rate formula.

<img width="193" alt="image" src="https://github.com/user-attachments/assets/dfe4cc86-b8bb-42fc-97df-a193cfa7401f">

**Step 6)** Analyzed and determined the **Top 3 Reasons for Customer Churn**.

![image](https://github.com/user-attachments/assets/435a4952-bf03-408b-8557-f653625845c1)

**Step 7)** Discover which **State Has the Highest Churn Rate** to identify regions needing targeted churn reduction strategies. Use map visualization to highlight results.

![image](https://github.com/user-attachments/assets/8ebda3a9-1ad1-46ea-9011-71ae24b0c6b5)

**Step 8)** **Key Insights Summary**
   - **Overall Churn Rate**: The total churn rate discovered is 26.86%.
   - **State with Highest Churn Rate**: The state with the highest churn rate is `California` with a churn rate of 63.24%.
   - **Top Reasons for Churn**: The primary factor driving customer churn is competition, indicating that adverse effects from competitors significantly contribute to customers leaving.

<img width="359" alt="image" src="https://github.com/user-attachments/assets/d0d0b62f-4d0e-4b9b-9683-c51c94b7a44d">

### *Churn Rate Analysis:*

**Step 9)** Churn Rate by Age Bins
- **Analysis:** The churn rate across age bins reveals patterns of customer retention and attrition.
- **Visualization:** Trend lines illustrate how age influences churn.

![image](https://github.com/user-attachments/assets/1773aa02-d5cc-46d2-b48e-c9a5a04f4916)

**Step 10)** Hypothesis Testing on Phone Bills
- **Hypothesis:** Lower phone bills in group customers contribute significantly to churn.
- **Outcome:** Statistical tests will verify or refute this correlation.
- **Visualization:** Displays the relationship between phone bills and churn rates.

![image](https://github.com/user-attachments/assets/cecf4c3b-6405-4601-b945-44306ddebfc8)

**Step 11)** Analysis of International Calling Behavior
- **Insight:** 72% of customers with international calling plans do not utilize them, indicating a potential area for improvement in customer engagement.
- **Visual Representation:** Highlights the discrepancy between plan availability and usage.

![image](https://github.com/user-attachments/assets/03bdf2d2-4373-47ee-9990-9514434c9763)

**Step 12)** Customer Validity and Payment Analysis
- **Focus Areas:**
  - **Customer Status:** Breakdown of active, inactive, and churned customers.
  - **Payment Methods:** Analysis of preferred payment methods among different customer statuses.
  - **Contract Types:** Comparison of monthly vs. yearly contracts.
- **Visualization:** Presents a comprehensive view of customer behavior related to validity and payment choices.

![image](https://github.com/user-attachments/assets/dc20a114-b408-4f7a-b585-72a95622edbb)












