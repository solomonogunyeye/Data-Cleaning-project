# Data-Cleaning-project

## Overview

This repository showcases practical data cleaning workflows across three real-world datasets of varying complexity. Each project demonstrates systematic approaches to transforming messy, inconsistent data into analysis-ready formats using Excel and Power Query. The focus is on data integrity, structural consistency, and scalable problem-solving techniques applicable to production environments.

---

# Project 1: Large-Scale Dataset Standardization

This project involves cleaning a high-volume dataset containing 9,000+ transactional records with widespread formatting inconsistencies, data type errors, and structural irregularities. The goal is to standardize all fields while maintaining 100% record accuracy, creating a foundation for reliable downstream processing.

## Objectives
1. Eliminate formatting inconsistencies across 9,000+ rows
2. Enforce correct data types for all columns
3. Remove unwanted symbols and hidden characters
4. Create clean dataset with uniform structure

## Dataset
| Detail | Info |
|---|---|
| **Source** | Internal business records |
| **Scope** | Multi-category transactional data |
| **Size** | 9,000+ rows · 12 columns |
| **Key Issues** | Mixed data types, irregular spacing, symbol contamination |

## Data Cleaning and Preprocessing
1. Verified zero missing values across all fields
2. Confirmed zero duplicate records
3. Applied `TRIM()` to remove leading/trailing spaces
4. Used `CLEAN()` to eliminate non-printable characters
5. Removed unwanted symbols via `SUBSTITUTE()` function
6. Converted text-stored numbers to proper numeric format
7. Standardized text casing across categorical fields

## Cleaning Results
- **Records processed:** 9,000+
- **Data type corrections:** 100% of numeric fields standardized
- **Text normalization:** All categorical columns cleaned
- **Formatting consistency:** 100%

## Key Outcomes
1. Formula-based cleaning reduced processing time by 85% compared to manual editing
2. Consistent data types enabled error-free calculations
3. Standardized structure ready for downstream tools

## Visual Documentation

| Before Cleaning | After Cleaning |
|----------------|----------------|
| 

![Before](images/project1_before.png)

 | 

![After](images/project1_after.png)

 |
| Inconsistent spacing, mixed symbols, irregular formatting | Uniform structure, clean standardized fields |

---

# Project 2: CSV Date & Text Standardization

This project focuses on resolving temporal inconsistencies and text formatting issues in a semi-structured CSV dataset. The dataset contained mixed date formats, inconsistent capitalization, and irregular spacing that prevented reliable time-based processing.

## Objectives
1. Standardize all date fields to uniform American (MDY) format
2. Normalize text casing for consistent processing
3. Validate date ranges for logical consistency
4. Prepare dataset for time-based operations

## Dataset
| Detail | Info |
|---|---|
| **Source** | CSV export from CRM system |
| **Scope** | Customer transaction records |
| **Key Issues** | Mixed date formats, inconsistent text casing |
| **Key Columns** | Transaction Date, Customer Name, Product Category |

## Data Cleaning and Preprocessing
1. Verified zero duplicate records
2. Detected three different date format patterns (MDY, DMY, YYYY-MM-DD)
3. Manually corrected 18 invalid date entries
4. Converted all dates to Excel native format
5. Applied `PROPER()` function to standardize customer names
6. Removed extraneous spaces from all text fields
7. Validated date ranges against business operational period

## Cleaning Results
- **Invalid dates corrected:** 18 entries
- **Date format consistency:** 100%
- **Text standardization:** All categorical fields normalized

## Key Outcomes
1. Manual validation required for 2.3% of records where automation would fail
2. Standardized dates enabled accurate time-series processing
3. Consistent text formatting eliminated duplicate category entries

## Visual Documentation

| Before Cleaning | After Cleaning |
|----------------|----------------|
| 

![Before](images/project2_before.png)

 | 

![After](images/project2_after.png)

 |
| Mixed date formats (MDY/DMY/ISO), inconsistent casing | Standardized MDY dates, proper case text |

---

# Project 3: Raw Text Transformation to Structured Data

This project involves transforming an unstructured plain-text file with inconsistent delimiters into a fully structured tabular dataset. The raw data lacked schema definition, contained multiple delimiter types, and required pattern-based parsing to extract meaningful fields.

## Objectives
1. Convert unstructured .txt file to structured tabular format
2. Identify and standardize inconsistent delimiters
3. Create proper column schema with descriptive headers
4. Validate field alignment and correct misplaced values

## Dataset
| Detail | Info |
|---|---|
| **Source** | Legacy system export |
| **Format** | Raw .txt file |
| **Size** | Variable row structure |
| **Key Issues** | Multiple delimiters (pipes, tabs, spaces), no headers, misaligned fields |

## Data Cleaning and Preprocessing
1. Imported .txt file into Power Query Editor
2. Analyzed delimiter patterns across all rows
3. Replaced inconsistent symbols (pipes, tabs, multiple spaces) with uniform commas
4. Split text by delimiter into distinct columns
5. Assigned descriptive column headers based on data context
6. Identified 23 misaligned values through pattern analysis
7. Manually reassigned misplaced values to correct columns
8. Validated final structure against source data samples

## Cleaning Results
- **Structure:** Unstructured text → 8-column table
- **Delimiter standardization:** 100%
- **Field alignment corrections:** 23 manual adjustments
- **Schema completeness:** Full header assignment

## Key Outcomes
1. Power Query enabled batch processing impractical with Excel formulas
2. Pattern-based validation identified systematic misalignments
3. Structured output ready for immediate integration

## Visual Documentation

| Before Cleaning | After Cleaning |
|----------------|----------------|
| 

![Before](images/project3_before.png)

 | 

![After](images/project3_after.png)

 |
| Unstructured raw text with irregular delimiters | Structured 8-column table with proper headers |

---

# Tools & Techniques

## Excel Functions
- **`TRIM()`** – Remove leading/trailing spaces
- **`CLEAN()`** – Eliminate non-printable characters  
- **`SUBSTITUTE()`** – Replace unwanted symbols
- **`PROPER()` / `UPPER()` / `LOWER()`** – Standardize text casing
- **Data Validation** – Enforce correct data types

## Power Query
- **Replace Values** – Batch symbol standardization
- **Split Column by Delimiter** – Text-to-columns transformation
- **Column Headers** – Schema definition
- **Manual Validation** – Pattern-based error correction

---

# Skills Demonstrated

| Skill Category | Specific Competencies |
|----------------|----------------------|
| **Scale** | Processing 9,000+ rows with formula-driven automation |
| **Data Types** | Text/number/date validation and enforcement |
| **Normalization** | Date format standardization, text casing consistency |
| **Transformation** | Unstructured-to-structured data conversion via Power Query |
| **Validation** | Manual verification for high-stakes corrections |
| **Tool Selection** | Excel formulas for structured data, Power Query for complex parsing |

---

# Methodology & Limitations

## Quality Assurance Approach
- **Formula-first:** Scalable functions applied before manual edits
- **Manual validation:** Critical fields verified when error cost exceeds automation benefit
- **Visual verification:** Before/after screenshots document all transformations

## Known Limitations
⚠️ **Project 2:** Some date corrections required human judgment to distinguish invalid formats from legitimate outliers  
⚠️ **Project 3:** Text restructuring relied on delimiter pattern consistency—irregular formats may require additional validation  
⚠️ **Trade-off:** Accuracy prioritized over speed in smaller datasets with high-stakes fields

---

# Repository Structure
