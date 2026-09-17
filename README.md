# ECE-2112-PA-4
Rivera, Francis Carlo E. | 2ECE-D

The repository covers Programming Assignment 4 for our ECE2112: Advanced Computer Programming and Algorithms course. The PA is divided into three programming problems that focuses on filtering tabular data through the selection of desired features that meet established Boolean criteria. Additionally, data analysis is conducted by creating labeled plots or figures for visualization.

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

The following commands were utilized in deriving the required data selections:
- `import pandas as pd` ---> Imports the Pandas library that contains indexing, subsetting, and slicing tools for data frame manipulation. The code converts the library name to the convention "pd".
- `board = pd.read_excel('board2.xlsx')` ---> Reads the excel file "board2.xslx" and converts it to a structured Pandas data frame assigned to the convention "board."
- `display(board)` ---> Displays the board data frame derived from the excel file board2.xslx.
- `VisComm = board.loc[(board['Hometown']=='Visayas')&(board['Track']=='Communication')]` ---> Filters the board data frame using Boolean conditions that extracts  the rows containing the following data: "Visayas" in their Hometown feature and "Communication" in their Track feature. The derived data frame is stored in "VisComm".
- `VisComm['Average']=VisComm[['Math', 'Electronics', 'GEAS', 'Communication']].mean(axis=1)` ---> Calculates the row-wise average of the data contained in the following features: Math, Electronics, GEAS, Communication. The code creates a new column called "Average" attached to the VisComm data frame where the calculated data averages are stored.
- `VisComm=VisComm[['Name', 'Gender', 'Math', 'Electronics', 'Average']]` ---> Filters the VisComm data frame by only retaining the following selected features: Name, Gender, Math, Electronics, Average.
- `display(VisComm)` ---> Displays the VisComm data frame.
- `print ('Number of Rows:', len(VisComm))` ---> Displays the number of rows of the finalized VisComm data frame.
```
import pandas as pd

board = pd.read_excel('board2.xlsx')
display(board)

VisComm = board.loc[(board['Hometown']=='Visayas')&(board['Track']=='Communication')]
VisComm['Average']=VisComm[['Math', 'Electronics', 'GEAS', 'Communication']].mean(axis=1)
VisComm=VisComm[['Name', 'Gender', 'Math', 'Electronics', 'Average']]
display(VisComm)
print ('Number of Rows:', len(VisComm))
```
# B. VISAYAS FEMALE DATAFRAME
> Objectives:
> - Create a second DataFrame named **"VisFemale"** containing students whose Hometown is Visayas and whose Gender is Female.
> - Retain only: **"Name, Track, GEAS, Electronics, Average"**.
> - Display VisFemale, then display only the rows of VisFemale whose Average is at least 60.
> - Do not overwrite VisFemale when performing this second filter.

The following commands were utilized in deriving the required data selections:
- `VisFemale = board.loc[(board['Hometown']=='Visayas')&(board['Gender']=='Female')]` --->  Filters the board data frame using Boolean conditions that extracts  the rows containing the following data: "Visayas" in their Hometown feature and "Female" in their Gender feature. The derived data frame is stored in "VisFemale".
- `VisFemale['Average']=VisFemale[['Math', 'Electronics', 'GEAS', 'Communication']].mean(axis=1)` ---> Calculates the row-wise average of the data contained in the following features: Math, Electronics, GEAS, Communication. The code creates a new column called "Average" attached to the VisFemale data frame where the calculated data averages are stored.
- `VisFemale=VisFemale[['Name', 'Track', 'GEAS', 'Electronics', 'Average']]` ---> Filters the VisFemale data frame by only retaining the following selected features: Name, Track, GEAS, Electronics, Average.
- `display(VisFemale)` ---> Displays the VisFemale data frame.
- `display(VisFemale.loc[VisFemale['Average']>=60])` ---> Filters the display selection of the VisFemale data frame using a Boolean condition that only selects rows whose data under the Average feature is 60 or above.

```
VisFemale = board.loc[(board['Hometown']=='Visayas')&(board['Gender']=='Female')]
VisFemale['Average']=VisFemale[['Math', 'Electronics', 'GEAS', 'Communication']].mean(axis=1)
VisFemale=VisFemale[['Name', 'Track', 'GEAS', 'Electronics', 'Average']]

display(VisFemale)
display(VisFemale.loc[VisFemale['Average']>=60])
```

# C. CATEGORY-AVERAGE VISUALIZATION
> Objectives: 
> - Examine how the recorded Average differs across the three categorical features **"Track, Gender, and Hometown"**.
> - a. For each feature, compute the mean of Average for every category using Pandas.
> - b. Display the three summary tables.
> - c. Create one figure containing three bar charts: **"mean Average by Track, by Gender, and by Hometown"**.
> - d. Below the figure, write three concise statements identifying the category with the highest sample mean for each feature.
> - Describe the observed dataset only (a difference in group means does not, by itself, establish that a feature causes a higher board-exam score).

The following commands were utilized in deriving required data selections and creating data figures:
- `Mean = board.copy()` --->
- `Mean['Average']=Mean[['Math', 'Electronics', 'GEAS', 'Communication']].mean(axis=1)`--->
- `Track_Average = Mean.pivot_table(index = 'Track', values = 'Average').reset_index()` --->
- `Gender_Average = Mean.pivot_table(index = 'Gender', values = 'Average').reset_index()` --->
- `Hometown_Average = Mean.pivot_table(index = 'Hometown', values = 'Average').reset_index()` --->
- `display(Track_Average)` --->
- `display(Gender_Average)` --->
- `display(Hometown_Average)` --->

### VERSION HISTORY
- September 14, 2026: README File created.
- September 14, 2026: Added content for introductory section.
- September 14, 2026: Added objectives for Part A, Part B, and Part C.
- September 17, 2026: Added content for Part A and Part B.
