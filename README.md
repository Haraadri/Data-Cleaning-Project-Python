# Data Cleaning with Python

## Objective:
The goal of this project was to clean and organize a raw dataset containing individual-level information, making it accurate, structured, and ready for analysis or modeling. In the real world, data is rarely perfect—it often contains missing values, errors, and inconsistencies that can lead to unreliable insights or flawed decision-making. This project aimed to address these challenges systematically, ensuring the dataset is reliable and suitable for practical use, whether in reporting, visualization, or predictive modeling.

## Why Data Cleaning is Important:
Data cleaning is a critical part of working with any dataset, whether for business or research purposes. High-quality, clean data is the foundation for making sound decisions and drawing meaningful conclusions. Here’s why data cleaning matters:

**1. Ensures Data Quality:**

- Cleaning removes inaccuracies, duplicates, and inconsistencies, making the dataset more trustworthy.

**2. Improves Analysis and Insights:**

- Reliable data leads to accurate results, reducing the risk of errors in statistical reports, dashboards, or predictive models.

**3. Prevents Misinterpretation:**

- Fixing issues like missing or invalid entries reduces the chance of drawing incorrect conclusions or making biased decisions.

**4. Streamlines Processes:**

- Clean data simplifies downstream workflows, saving time in analysis, visualization, or machine learning projects.

**5. Supports Informed Decision-Making:**

- With a clean and complete dataset, insights are more reliable, enabling better strategies and actions.

This project tackled common data quality issues head-on, transforming a messy dataset into a ready-to-use resource for professional tasks. Clean data not only ensures accurate results but also saves time and resources in future steps, making it an essential part of any data-driven process.

## Steps Taken to Clean the Data:

### 1. Initial Data Review

I started by understanding the dataset, which had 20 rows and 10 columns, covering personal details like first name, last name, height, weight, and spending data from three supermarkets (Spend_A, Spend_B, Spend_C).

**Issues Identified**:
- The Age_Sex column combined two pieces of information, requiring splitting into separate Age and Sex columns.
- Missing values were inconsistently represented as NaN, "xx," or blanks, normalized, and filled using the mean.
- Negative and unrealistic values, such as negative weights, spending amounts, and a height of 0 cm, were identified and corrected.
- Numerical columns like Spend_C and Weight(kg) were stored as text, requiring conversion for calculations.
- Outliers, such as a weight of 153 kg, were corrected based on logical assumptions (e.g., replacing it with 53 kg).

### 2. Cleaning Process

**2.1 Handling Missing and Invalid Data**
- Converted invalid entries (e.g., "xx") into NaN using Python’s pd.to_numeric() with the errors='coerce' argument.
- Checked all columns for missing data using commands like df.isnull().sum(). Missing values were filled using the mean value of the respective columns to retain the dataset’s structure.

**2.2 Splitting and Reordering Columns**
- The Age_Sex column was split into two separate columns: Age and Sex, making the data easier to analyze.
- Removed the original Age_Sex column and reordered all columns for logical clarity.

**2.3 Addressing Negative and Unrealistic Values**
- Replaced negative values in the weight column (e.g., -60) with their positive equivalents (e.g., 60).
- Adjusted outliers like 0 in the height column by replacing them with the mean height of the dataset.
- Replaced a high outlier (153 kg) in the weight column, assumed to be a typo, with 53 kg.
- Similarly, corrected negative values in spending columns like -220 in Spend_B to 220.

**2.4 Ensuring Proper Data Types**
- Changed text-based columns to numerical types where required (e.g., Spend_C was converted to a numeric column).
- Used the df.dtypes command to verify appropriate data types for all columns.

### 3. Validating the Clean Data

- Ensured there were no missing values left using assertions. These statements confirmed that all data entries were valid and non-missing.
- Verified that all numerical columns contained only positive numbers.

### 4. Final Adjustments

- Rounded all numerical values to two decimal places for better readability and consistency.

## Key Findings After Cleaning:

**1. Improved Data Structure:**
- The dataset now has logical and clean column labels with clear separation of information.
- Proper column ordering improved dataset readability.

**2. Error Resolution:**
- All missing values were addressed by filling them with mean values.
Invalid and unrealistic entries, like negative weights and spending amounts, were corrected.
- Data types were fixed for all columns, ensuring consistent numerical and textual formats.

**3. Enhanced Usability:**
- The cleaned dataset is free of errors, inconsistencies, and outliers, making it ready for use in further analysis or predictive modeling.

## Conclusion:
This project successfully transformed a messy, error-filled dataset into a clean, structured, and reliable resource ready for analysis and modeling. By systematically addressing issues such as missing values, invalid entries, data type mismatches, and outliers, the dataset is now in a format that ensures accurate results and meaningful insights.

Key takeaways from the project include:

**1. Improved Data Integrity:**

- The dataset is now free of errors, with all missing values filled appropriately, and all inconsistencies resolved. Numerical columns are correctly formatted, and outliers have been managed effectively.

**2. Enhanced Usability:**

- The dataset has been restructured for better readability, with logical column arrangements and consistent formatting, making it more accessible for analysis or reporting.

**3. Reliable Insights:**

- Cleaning the data ensures that any analysis performed on it will be accurate and trustworthy, supporting better decision-making and reducing the risk of errors in downstream processes.

**4. Foundation for Future Tasks:**

- With a well-prepared dataset, subsequent steps such as statistical modeling, machine learning, or business analysis will require less effort, saving both time and resources.

In professional practice, clean data is not just a "nice-to-have" but a necessity. Poor-quality data can lead to wasted effort, unreliable conclusions, and flawed decisions. This project highlights the importance of dedicating time and attention to cleaning and preparing data before diving into deeper analysis or model-building.

Ultimately, this work ensures the dataset is ready to support its intended purpose—whether for generating insights, building predictive models, or informing business strategies—helping to unlock the full potential of the data.
