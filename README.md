## Project Overview

This project demonstrates the process of **extracting, cleaning, transforming, and preparing web-scraped data using Microsoft Excel Power Query**.

The dataset contains the **2020 Summer Olympics medal table**, which was extracted from Wikipedia and then cleaned and transformed in Power Query to make it suitable for further analysis.

## Project Objective

The main objectives of this project were to:

- Extract Olympics medal data from a web source
- Import the data into Power Query
- Clean and standardise the dataset
- Handle missing/shared ranking values
- Correct data types
- Create a calculated metric
- Remove unnecessary records
- Prepare the final dataset for analysis

## Data Source

The data was extracted from:

**2020 Summer Olympics Medal Table – Wikipedia**

https://en.wikipedia.org/wiki/2020_Summer_Olympics_medal_table

The data was extracted using the **From Web** functionality in Excel Power Query.

## Tools Used

- Microsoft Excel
- Power Query
- Web Data Extraction
- Data Cleaning & Transformation

## Data Cleaning & Transformation Process

### 1. Extract Data from Web

The Olympics medal table was extracted from the Wikipedia webpage using:

**Excel → Data → Get Data → From Web**

The extracted data was then opened in the Power Query Editor.

### 2. Rename Column

The `NOC` column was renamed to:

`Country`

### 3. Clean Country Names

The `*` character appearing in the Country column was removed using:

**Transform → Replace Values**

`*` → blank

### 4. Fill Missing Rank Values

The Rank column contained blank cells where countries shared the same rank.

The following Power Query operation was used:

**Transform → Fill → Down**

### 5. Change Data Types

The medal-count columns were converted from **Text** to **Whole Number**.

This allows the medal values to be used correctly in calculations.

### 6. Calculate Gold Medal Percentage

A new calculated column was created using:

**Gold Medals ÷ Total Medals**

The resulting column was then converted to **Percentage** format.

### 7. Remove Unnecessary Total Row

The overall totals row was removed because the analysis focuses on individual countries.

### 8. Rename Dataset

The dataset name was changed from:

`2020 Summer Olympics medal table[35]`

to:

`medals`

### 9. Load the Cleaned Data

After completing the transformations:

**Home → Close & Load**

was used to load the cleaned dataset into Excel.

# Before & After Data Cleaning

## Before Cleaning

The following screenshot shows the dataset immediately after extracting it from the web, before applying the cleaning and transformation steps.

![Unclean Data](Unclean%20Data%20from%20Web.png)

## After Cleaning

The following screenshot shows the dataset after applying the Power Query cleaning and transformation steps.

![Cleaned Data](Data%20after%20cleaning.png)
