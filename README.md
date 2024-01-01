
# FIFA 21 Dataset Cleaning and Exploration

## Overview
This Python project delves into the meticulous cleaning and exploration of the FIFA 21 dataset, employing robust data analysis techniques powered by Pandas and NumPy. The objective is to ensure the dataset is primed for in-depth analysis, revealing valuable insights into the characteristics of FIFA 21 players.

[Link to Dataset](https://www.kaggle.com/datasets/yagunnersya/fifa-21-messy-raw-dataset-for-cleaning-exploring)

## Key Objectives

### 1. Data Cleaning
The project places a strong emphasis on data integrity, employing various techniques to enhance the overall quality of the dataset:

- **Handling Duplicates:** Rigorous identification and removal of duplicate rows to maintain data accuracy.
- **Column Optimization:** Strategic removal of unnecessary columns ('Name', 'photoUrl', 'playerUrl') for streamlined analysis.
- **Handling Missing Values:** Implementation of effective strategies to address and rectify missing values in key columns.

### 2. Numeric Conversion
Ensuring the dataset is equipped for numerical analysis by transforming relevant columns into appropriate numeric formats:

- **Weight and Height:** Conversion of 'Weight' from pounds to kilograms and 'Height' from centimeters to meters, facilitating standardized numerical analysis.
- **Hits, Value, Wage, Release Clause:** Precision in converting these columns to numeric formats, establishing a solid foundation for subsequent quantitative analysis.

### 3. Data Exploration
Leveraging the power of Pandas and NumPy, the project embarks on a detailed exploration of FIFA 21 player data:

- **Statistical Analysis:** Utilization of Pandas for statistical insights into player attributes and performance metrics.


## Code Highlights

```python
# Sample code snippet showcasing data loading, cleaning, and exploration
import pandas as pd
import numpy as np

# Load the dataset
df = pd.read_csv("your_dataset.csv", sep=',')

# Drop unneeded columns
columns_to_drop = ['Name', 'photoUrl', 'playerUrl']
df.drop(columns=columns_to_drop, inplace=True)

# Rename 'LongName' column
df.rename(columns={'LongName': 'Name'}, inplace=True)
display(df.head(5))
