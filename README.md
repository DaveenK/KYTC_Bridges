Daveen Knue
August 2023 Data Analysis - Code Kentucky
KYTC BRIDGE DATA ANALYSIS
I analyzed KYTC's bridge data in hopes to better understand what kinds of bridges there are in Kentucky and how much is being spent on them over time.

DATA WRANGLING:
The general bridge data, Ky_Bridge_Points.csv came from https://opengisdata.ky.gov/ which formatted the data into a csv for me. The bridge weight limit data, Kentuckys Weight-Posted Bridges.csv came as an excel file from https://datamart.kytc.ky.gov/. I opened the excel file in Google Sheets, deleted the first empty row and resaved it as a csv. I did the same with KYTC Project Archives.csv, the data on KYTC Projects from 2007  - Present, which came from https://transportation.ky.gov/Construction-Procurement/Pages/default.aspx. I also used Sheets to get rid of the '$' from project costs. I did this for these two excel files, because, when I opened them with pandas, and tried to format them that way, it was not working appropriately, even with the help of ChatGPT. 



WAYS PROJECT COULD BE IMPROVED:
The KYTC Project Archives do not include the Bridge IDs so unfortunately this table could not be joined with the others.
Unfortunately, public data on bridge conditions was not available prior to project duedate.