# Daveen Knue - August 2023 Data Analysis - Code Kentucky
## KYTC BRIDGE DATA ANALYSIS
#### Disclaimer: This analysis of KYTC bridge data is not affiliated with KYTC.  

### OVERVIEW:
Using Python and pandas, I analyzed KYTC's bridge data from 2007 - 2023 in hopes to better understand what kinds of bridges there are in Kentucky and how much was being spent on them over the 16-year time period.  

### DATA WRANGLING:
The general bridge data, Ky_Bridge_Points.csv came from https://opengisdata.ky.gov/ which formatted the data into a csv for me. The bridge weight limit data, Kentuckys Weight-Posted Bridges.csv came as an excel file from https://datamart.kytc.ky.gov/. I opened the excel file in Google Sheets, deleted the first empty row and resaved it as a csv. I did the same with KYTC Project Archives.csv, the data on KYTC Projects from 2007  - 2023, which came from https://transportation.ky.gov/Construction-Procurement/Pages/default.aspx. I also used Sheets to get rid of the '$' from project costs. I did this for these two excel files, because, when I opened them with pandas, and tried to format them that way, it was not working appropriately, even with the help of ChatGPT. 
  
When reading in Ky_Bridge_Points.csv, I received a dtype error for columns 62 and 64. Originally I converted the dtypes to int, but those columns are not needed for this analysis, so, ultimately, I dropped the columns instead.  

### FEATURES  
#### 1. Loading data
- Read two data files.
#### 2. Clean and operate on the data while combining them
- Clean your data and perform a pandas merge with your two data sets, then calculate some new values based on the new data set.
#### 3. Visualize / Present your data
- Make 3 matplotlib visualizations to display your data.
#### 4. Best practices
- Utilize a virtual environment and include instructions in your README on how the user should set one up.

### TECHNICAL INSIGHT:
**Environment:** I used a venv and a Jupyter Notebook in Visual Studio Code to document and track my progress.  
**Python Libaries:** I used pandas, matplotlib and datetime for wrangling, cleaning and analyzing data.  
**Data Sources:** The bridge data for this analysis was sourced from the Kentucky Transportation Cabinet (KYTC) in CSV format.  
**Access Requirements:** No special access is required, because the data is openly provided by KYTC.  
**Data Visualization:** I used matplotlib to create bar graphs, tables and a line graph to display the bridge data in a format easier to read.  
**Reporting:** Prepare a report/presentation summarizing key findings, insights, and visual outputs from the analysis.  
  
### PYTHON VIRTUAL ENVIRONMENT (venv) SET-UP:
I. Make sure you have Python installed. If not, download and install it from python.org. This project utilizes Python 3.11.5.

II. Using GitBash in your terminal, clone the repo to your machine and then navigate to the project folder.  
`git clone https://github.com/DaveenK/KYTC_Bridges.git`  
`cd path/to/the/project/folder`

III. Create a venv in the project folder:  
`python -m venv example_venv`

IV. Activate the venv:  
`source example_venv/Scripts/activate`

V. Install the required packages:  
`pip install -r requirements.txt`

VI. When you are finished working on the repo, deactivate the venv:  
`deactivate`

### WAYS PROJECT COULD BE IMPROVED:
- The KYTC Project Archives do not include the Bridge IDs so unfortunately this dataframe could not be joined with the others.
- Unfortunately, public data on bridge conditions was not available prior to project duedate.