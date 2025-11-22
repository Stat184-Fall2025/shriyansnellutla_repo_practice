This document contains the full plan for Activity 15 analysis and the creation and maintenance of the GitHub repo that stores work

Project Goals:
- To tidy the Armed Forces data and join it with rank data to create two cleaned datasets:
- a grouped dataset where each row represents a branch/sex/pay grade group,
- and an individual-level dataset using uncount().
- Additionally, to complete the remaining work required for Activity 14,
- including the Baby Names time-series visualization (Activity #13),
-  the mathematical function plot (Activity #04), and the written reflection section.
-  Finally, to organize all files in a GitHub repository that demonstrates proper version control through branches, issues, commits, pull requests, a README, and a plan document.

Needs: 
- The Armed Forces and Rank datasets
- Baby Names dataset from {dcData} packages
- R {tidyverse,rvest,googlesheets4,ggplot2,Quarto, dcData}

Steps: 
1)Load all necessary packages, including tidyverse,rvest,googlesheets4,ggplot2, and dcData
2)For Pay Grade and Rank Table:
- Extract the appropriate tables
- Fix column headers 
- Remove footer rows
- Reshape from wide to long
- Convert -- to NA
3) Load Armed Forces
  - Load main body of sheet without headers
  - Assign correct names
4) Wrangle Armed Forces
- Rename columns to a better name
- Remove total columns/rows
- Reshape to long form where Frequency becomes a single variable
- Separate branch and sex
- Parse counts to numeric values
5) Merge Rank and Force
- Join cleaned Armed Forces with cleaned rank using Pay Grade and Branch
6) Transform Groups to Rows
  - Use uncount with Frequency to expand grouped data
7) Visualize
- Filter the dataset to Army enlisted personnel
- Create 2-way Frequency tables of Rank and Sex
- use knitr::kable()
- Write narraitve text
8) Baby Names Vizualstion
  - Load baby names from {dcData}
  - Filter for Emma and Liam
  - Create a time series line plot of name counts over time
  - Write narrative text explaining patterns and changes
9) Math Function Plot
- Define a volume function for the open top box
- Use stat_function() to plot volume vs cut-out length
- Write a narrative text explaining the shape of the curve and the best x-value
10) Render Doc
- Render QMD to a PDF using Quarto 
  
  
