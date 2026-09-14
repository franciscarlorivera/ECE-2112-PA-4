# ECE-2112-PA-4
Rivera, Francis Carlo E. | 2ECE-D

The repository covers Programming Assignment 4 for our ECE2112: Advanced Computer Programming and Algorithms course. The PA is divided into three programming problems that focuses on filtering tabular data through the selection of desired features that meet established Boolean criteria. Additionally, data comparison is conducted by creating labeled plots or figures for visualization.

## INTENDED LEARNING OUTCOMES
1. Filter tabular data using several categorical and numerical conditions
2. Construct focused DataFrames by selecting relevant features
3. Summarize the relationship between categorical features and a numerical variable
4. Communicate a data comparison using clear and correctly labeled plots

# A. VISAYAS COMMUNICATION DATAFRAME
> Objectives: 
> - Create a DataFrame named **"VisComm"** containing students whose Hometown is Visayas and whose Track is Communication.
> - Retain only these columns, in the stated order: **"Name, Gender, Math, Electronics, Average"**.
> - Display the resulting DataFrame and its number of rows.
> - Both filtering conditions must be applied to the source dataset before the columns are selected.


# B. VISAYAS FEMALE DATAFRAME
> Objectives:
> - Create a second DataFrame named **"VisFemale"** containing students whose Hometown is Visayas and whose Gender is Female.
> - Retain only: **"Name, Track, GEAS, Electronics, Average"**.
> - Display VisFemale, then display only the rows of VisFemale whose Average is at least 60.
> - Do not overwrite VisFemale when performing this second filter.


# C. CATEGORY-AVERAGE VISUALIZATION
> Objectives: 
> - Examine how the recorded Average differs across the three categorical features **"Track, Gender, and Hometown"**.
> - a. For each feature, compute the mean of Average for every category using Pandas.
> - b. Display the three summary tables.
> - c. Create one figure containing three bar charts: **"mean Average by Track, by Gender, and by Hometown"**.
> - d. Below the figure, write three concise statements identifying the category with the highest sample mean for each feature.
> - Describe the observed dataset only (a difference in group means does not, by itself, establish that a feature causes a higher board-exam score).


### VERSION HISTORY
- September 14, 2026: README File created.
- September 14, 2026: Added content for introductory section.
- September 14, 2026: Added objectives for Part A, Part B, and Part C.
