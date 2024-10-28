
# Analyzing Customer Churn in POWER BI

- Churn Definition : The churn rate, also known as the rate of attrition or customer churn, is the rate at which customers stop doing business with an entity. There are multiple ways to calculate churn and it varies across the industries.
- Simplified Formula : Churn rate = customers lost / total number of customers
- Attrition typically refers to the gradual reduction in the number of people, employees, or customers over time. In a business context, it often describes the rate at which employees leave a company or customers stop engaging with a business.
## Overview :

We'll analyze the ficticous dataset from a Telecom Provide (Databel), to discover why customers are churning? 

The Basic data analysis flow implemented: 
- Data Check
- Explore Data
- Analyze and Visualize data 
- Dashboarding




## Link to Dataset

 - [DataBel Telecom Dataset](https://github.com/PriyaSree13/DataBel-Customer-Churn-/blob/main/Databel%20-%20Data.csv)





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

### Subscription Types & Charges

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




