# Layoffs Data Cleaning Project | MySQL

## Project Overview

This project focuses on cleaning and standardizing a layoffs dataset using MySQL to improve data quality and prepare the data for reliable analysis.

The project follows a structured data-cleaning workflow involving duplicate detection, text standardization, date formatting, missing-value investigation, industry classification corrections, and removal of unnecessary columns.

Using SQL queries, Common Table Expressions (CTEs), window functions, and data manipulation statements, the project demonstrates how raw and inconsistent data can be transformed into a more structured and analysis-ready dataset.

## Project Objectives

- Identify and remove duplicate records.
- Standardize company names, industry classifications, and country values.
- Convert date fields into a consistent DATE format.
- Investigate missing values across important columns.
- Correct inconsistent industry classifications where appropriate.
- Remove records with missing layoff figures when both total layoffs and layoff percentages are unavailable.
- Prepare a cleaned dataset for subsequent exploratory data analysis.

## Data Cleaning Workflow

1. **Data Staging:** Created staging tables to preserve the original dataset while performing cleaning operations.
2. **Duplicate Detection:** Used ROW_NUMBER() and CTEs to identify duplicate records.
3. **Text Standardization:** Applied TRIM() and UPDATE statements to clean company names and standardize industry values.
4. **Date Formatting:** Converted text-based dates into a consistent DATE data type using STR_TO_DATE().
5. **Missing-Value Handling:** Investigated missing industry and layoff information and applied corrections where appropriate.
6. **Data Validation:** Queried distinct values and selected company records to investigate inconsistencies.
7. **Final Preparation:** Removed identified duplicate rows, excluded records missing both layoff measures, and dropped the temporary row-number column.

## Tools & Technologies

- MySQL
- SQL Data Cleaning
- Common Table Expressions (CTEs)
- Window Functions
- ROW_NUMBER()
- String Functions
- Date Conversion Functions
- UPDATE, DELETE, ALTER TABLE
- Data Quality Checks

## Project Outcome

The project establishes a structured workflow for improving the consistency and usability of layoffs data. The cleaned dataset can serve as a foundation for further analysis of layoffs by company, industry, country, funding stage, and date.


## Technical Implementation

### Data Staging
- Created staging tables using CREATE TABLE LIKE.
- Copied source data into staging tables for cleaning.
- Used SELECT statements to inspect records and validate transformations.

### Duplicate Handling
- Applied ROW_NUMBER() with PARTITION BY to identify potential duplicate records.
- Used CTEs to isolate duplicate rows.
- Removed records marked as duplicates from the secondary staging table.

### Data Standardization
- Used TRIM() to remove unwanted whitespace.
- Standardized industry labels using UPDATE statements and pattern matching.
- Investigated inconsistencies in country and company values.

### Missing-Value Management
- Identified records with missing industry classifications.
- Investigated missing layoff figures.
- Removed records where both total_laid_off and percentage_laid_off were NULL.

### Date Transformation
- Used STR_TO_DATE() to convert text dates into SQL date values.
- Modified the date column to use the DATE data type.

### Final Data Preparation
- Removed the temporary row_num column.
- Organized the cleaned data for subsequent exploratory analysis.

## SQL Concepts Demonstrated

CREATE TABLE, INSERT INTO, SELECT, UPDATE, DELETE, ALTER TABLE, TRIM(), LIKE, STR_TO_DATE(), IS NULL, Common Table Expressions (CTEs), ROW_NUMBER(), PARTITION BY, and data type conversion.
