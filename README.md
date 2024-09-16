# Customer Data Analysis for Insurance Premium Discounts

## Project Overview
This project analyzes customer and policy data from an insurance company to identify candidates for premium discounts. The main objectives were to clean and prepare the data, analyze it for meaningful insights, and discover potential relationships that influence premium costs.

## Data Description
The dataset is organized into two main tables:
- **Customer Details**: Contains personal and vehicular information of the customers.
- **Customer Policy Details**: Contains details related to the insurance policies of the customers.

### Attributes:
- **Customer Details**:
  - customer_id
  - Gender
  - age
  - driving license presence
  - region code
  - previously insured
  - vehicle age
  - vehicle damage
- **Customer Policy Details**:
  - customer_id
  - annual premium
  - sales channel code
  - vintage
  - response

## Data Cleaning and Preprocessing
### Tasks Performed:
- **Adding Column Names**: Added proper headers to both datasets.
- **Handling Null Values**:
  - Dropped null values for 'customer_id'.
  - Replaced null values in numeric columns with their mean.
  - Filled null values in categorical columns with the mode.
- **Outlier Treatment**:
  - Identified and replaced outliers in numeric columns using the IQR method.
- **Normalization of Text Data**:
  - Removed any white spaces and standardized text to lower case.
- **Categorical Encoding**:
  - Converted categorical data into dummy variables for future modeling.
- **Duplicate Records**:
  - Removed any duplicate entries to ensure data integrity.

## Data Merging
Created a master table by merging customer details with policy details using 'customer_id', enabling a comprehensive view for analysis.

## Analysis and Insights
### Conducted Analyses:
- **Premium Analysis**:
  - Computed gender-wise and age-wise average annual premiums.
  - Analyzed the impact of vehicle age on average premiums.
- **Gender Distribution Check**:
  - Evaluated if the dataset is balanced across genders.
- **Correlation Analysis**:
  - Explored the relationship between a person's age and their annual premium.

## Key Findings
- Provided insights on how gender, age, and vehicle age influence premium amounts.
- Assessed the balance of gender distribution within the data.
- Identified the strength of the relationship between age and premium rates.

## Technologies Used
- **Python**
- **Pandas**: Data manipulation
- **Matplotlib/Seaborn**: Data visualization

## Challenges Faced
## Data Cleaning and Preprocessing Challenges

### Null Value Treatment
- Handling null values was challenging, particularly in deciding whether to use the mean or mode for replacement. Identifying the most appropriate strategy for columns like 'age' and 'annual premium' required careful analysis to maintain data integrity without skewing the dataset.
- Dropping null values in the 'customer_id' field was straightforward due to its nature as a unique identifier. However, ensuring that no associated data was inadvertently lost required careful validation.

### Outlier Detection and Treatment
- Outlier detection using the IQR method presented challenges, especially in determining the best approach to handle extreme values without distorting the underlying trends in data such as 'annual premium'. Deciding whether to remove outliers or replace them with the mean necessitated multiple iterations to find the right balance between data fidelity and robust statistical analysis.
- Specific cases, such as outliers in the 'vintage' column, needed tailored approaches since these values represent customer loyalty duration, which is critical to understanding customer behavior but was skewed by a few extremely high values.

### Data Inconsistency
- Certain rows showed inconsistency in data types, especially in columns where numeric values were expected, but strings were found. For example, the 'region code' column occasionally contained mixed types due to input errors, complicating automated processing.
- Handling mixed data types in the 'vehicle damage' column (entries sometimes recorded as yes/no or true/false) required standardization before further analysis could be conducted effectively.

### Handling Categorical Data
- Converting categorical data into a format suitable for modeling, particularly with nominal data in 'vehicle damage' and 'previously insured' columns, involved creating dummy variables. Deciding on the encoding technique (one-hot vs. label encoding) required consideration of the model’s requirements and potential impacts on performance.

### Specific Instances of Data Challenges
- Anomalies in 'annual premium' data for some entries, like customer_id '12345', where the premium was exceptionally high relative to the general customer base, prompted a deeper investigation into potential data entry errors or unique circumstances justifying these outliers.
- A significant challenge was encountered with customer_id '67890', where multiple conflicting records were present, likely due to data duplication or entry errors, complicating the cleaning process and necessitating a detailed review and manual corrections.

## Conclusion and Future Work
- Summarized the impact of the findings on the company's decision-making process regarding premium discounts.
- Proposed future analyses, like detailed customer segmentation or predictive modeling to forecast customer behaviors.

## How to Run
To run this project, ensure you have Python and necessary packages installed, then execute the Jupyter notebooks within the provided environment.

## License
This project is licensed under the MIT License - see the LICENSE.md file for details.
