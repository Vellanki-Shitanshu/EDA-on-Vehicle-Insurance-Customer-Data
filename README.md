Customer Data Analysis for Insurance Premium Discounts
Project Overview
This project analyzes customer and policy data from an insurance company to identify candidates for premium discounts. The main objectives were to clean and prepare the data, analyze it for meaningful insights, and discover potential relationships that influence premium costs.

Data Description
The dataset is organized into two main tables:

Customer Details: Contains personal and vehicular information of the customers.
Customer Policy Details: Contains details related to the insurance policies of the customers.
Attributes:
Customer Details:
customer_id
Gender
age
driving license presence
region code
previously insured
vehicle age
vehicle damage
Customer Policy Details:
customer_id
annual premium
sales channel code
vintage
response
Data Cleaning and Preprocessing
Tasks Performed:
Adding Column Names: Added proper headers to both datasets.
Handling Null Values:
Dropped null values for 'customer_id'.
Replaced null values in numeric columns with their mean.
Filled null values in categorical columns with the mode.
Outlier Treatment:
Identified and replaced outliers in numeric columns using the IQR method.
Normalization of Text Data:
Removed any white spaces and standardized text to lower case.
Categorical Encoding:
Converted categorical data into dummy variables for future modeling.
Duplicate Records:
Removed any duplicate entries to ensure data integrity.
Data Merging
Created a master table by merging customer details with policy details using 'customer_id', enabling a comprehensive view for analysis.

Analysis and Insights
Conducted Analyses:
Premium Analysis:
Computed gender-wise and age-wise average annual premiums.
Analyzed the impact of vehicle age on average premiums.
Gender Distribution Check:
Evaluated if the dataset is balanced across genders.
Correlation Analysis:
Explored the relationship between a person's age and their annual premium.
Key Findings
Provided insights on how gender, age, and vehicle age influence premium amounts.
Assessed the balance of gender distribution within the data.
Identified the strength of the relationship between age and premium rates.
Technologies Used
Python
Pandas: Data manipulation
Matplotlib/Seaborn: Data visualization
Challenges Faced
Discuss challenges encountered during data cleaning, such as outlier handling and null value treatment.
Mention specific instances where data inconsistency was a significant challenge.
Conclusion and Future Work
Summarized the impact of the findings on the company's decision-making process regarding premium discounts.
Proposed future analyses, like detailed customer segmentation or predictive modeling to forecast customer behaviors.
How to Run
To run this project, ensure you have Python and necessary packages installed, then execute the Jupyter notebooks within the provided environment.

License
This project is licensed under the MIT License - see the LICENSE.md file for details.
