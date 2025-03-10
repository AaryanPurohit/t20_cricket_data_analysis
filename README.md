# 🏏 Cricket Team Analyzer: T20 World Cup 2022  
**Project Sportan**  
*"Selecting the Best 11 Players on the Planet"*  

---

## 📌 Project Overview  
This project identifies the **optimal T20 World Cup 2022 squad** by analyzing player performance against role-specific parameters. The goal is to build a team that:  
- **Scores 180+ runs** on average.  
- **Defends 150 runs** on average.  

Players are evaluated across five roles: **Openers**, **Middle Order**, **Finishers**, **All-Rounders**, and **Specialist Fast Bowlers**, using metrics like batting average, strike rate, and bowling economy.  

---

## ⭐ Features   
- **Interactive Power BI Dashboard**: Explore players using dynamic filters and visualizations like scatter plots, heatmaps, and radar charts.  
- **Role-Specific Player Evaluation**: Assess players for 5 roles with predefined parameters:  
  - **Openers**: Batting Avg >30, Strike Rate >140, Boundary % >50  
  - **Middle Order**: Batting Avg >40, Strike Rate >125, Avg. Balls Faced >20  
  - **Finishers**: Batting Avg >25, Strike Rate >130, Batting Position >4  
  - **All-Rounders**: Batting Avg >15, Strike Rate >140, Bowling Economy <7  
  - **Specialist Fast Bowlers**: Economy ≤7, Dot Ball % >40, Innings Bowled >4  
- **Real-Time Projections**: Instantly calculates team's projected average score (180+ runs) and defense capability (150 runs).  
- **Drag-and-Drop Team Builder**: Visually assemble your final 11 by selecting top performers from each role.  

---

## 🚀 Steps to Build the Project  

### 1. **Data Collection**  
- **Web Scraping**:  
  - Collected raw T20 data (batting, bowling, match results) from **ESPN Cricinfo** using Python libraries:  
    - `Beautiful Soup` for parsing HTML.  
    - `Scrapy` for structured data extraction.  
  - Stored scraped data in **JSON format** for initial processing.  

### 2. **Data Preprocessing**  
- **Cleaning & Structuring**:  
  - Converted JSON files to structured **CSV datasets** using `pandas` and `numpy`.  
  - Removed irrelevant columns, fixed formatting errors, and standardized player/match IDs.  
  - Processed three key datasets:  
    - `Batting Summary` (runs, strike rate, boundaries).  
    - `Bowling Summary` (economy, wickets, dot balls).  
    - `Match Results` (team scores, venues, dates).  
  - Linked files using SQL for consistency (e.g., joining player IDs across tables).  

- **Filtering & Aggregation**:  
  - Applied **SQL queries** to filter players with sufficient innings (e.g., `SELECT * FROM players WHERE innings > 5`).  
  - Aggregated metrics like average runs, strike rate, and economy.  
  - Final output: Cleaned CSV files ready for analysis.  

### 3. **Dashboard Development**  
- **Power BI Setup**:  
  - Loaded CSV files into **Power BI** and refined data using **Power Query**:  
    - Added calculated columns (e.g., `Boundary %`, `Dot Ball %`).  
    - Merged tables for cross-metric analysis.  
  - **DAX Implementation**:  
    - Created metrics like `Batting Avg`, `Bowling Strike Rate`, and `Player Selection` flags.  
    - Example:  
      ```dax  
      Batting Avg = DIVIDE([Total Runs], [Total Innings Dismissed], 0)  
      ```  
  - **Visualizations**:  
    - Built interactive charts (bar, scatter), matrices, and heatmaps.  
    - Designed role-specific tabs for Openers, Middle Order, etc.  

### 4. **Team Selection**  
- **Role-Specific Shortlisting**:  
  - Applied criteria from `Parameter Scoping.pdf` (e.g., Openers: `Strike Rate > 140`).  
  - Filtered top performers using Power BI slicers and SQL-backed metrics.  
- **Team Builder Panel**:  
  - Assembled the final 11 using a drag-and-drop interface.  
  - Validated team balance against goals:  
    - Projected **180+ average score**.  
    - Ability to defend **150 runs**.  


---

## 🛠️ Technologies Used  
- **Data Collection**: Python (BeautifulSoup, Scrapy)  
- **Preprocessing**: Jupyter Notebook, Pandas, Power Query, SQL  
- **Analysis & Visualization**: Power BI, DAX  
- **Version Control**: Git, GitHub  

---

## 📊 Role-Specific Criteria  
| **Role**               | Batting Avg | Strike Rate | Key Metrics                          |  
|------------------------|-------------|-------------|--------------------------------------|  
| **Openers**            | >30        | >140        | Boundary % >50%                      |  
| **Middle Order**       | >40        | >125        | Avg. Balls Faced >20                 |  
| **Finishers**          | >25        | >130        | Batting Position >4, Balls Faced >12|  
| **All-Rounders**       | >15        | >140        | Bowling Economy <7, SR <20          |  
| **Specialist Bowlers** | -          | -           | Economy ≤7, Dot Ball % >40%         |  

---

## 📈 Dashboard Images 

**Power Hitters/ Openers**
![image](https://github.com/user-attachments/assets/a7719d9c-119e-404f-a48d-f01327c3ed84)

**Combined performance of Virat Kohli and Suryakumar Yadav as an anchor**

![image](https://github.com/user-attachments/assets/22b6ea8e-b34b-47e7-a1d9-628056f6cd35)

**Finisher**

![image](https://github.com/user-attachments/assets/7bd2859a-0424-4408-a8af-5acc763a7ff9)

**All Rounders**

![image](https://github.com/user-attachments/assets/f62e48e9-0051-41ae-9dd8-54714162777e)

**Combined performance of Sam Curran and Shaheen Afridi as a Specialist Fast Bowlers**

![image](https://github.com/user-attachments/assets/1ba1dae7-52fb-41f3-935a-1f6be8210cd6)



**Final 11**
![image](https://github.com/user-attachments/assets/8717c23f-0e60-4926-9bc1-812253006b9d)





---


This README provides a structured, detailed guide to your project. Adjust links, filenames, and sections to match your repository! 🏆

## 🔗 Connect 
[![GitHub](https://img.shields.io/badge/GitHub-Profile-blue?logo=github)](https://github.com/AaryanPurohit)  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/aaryan-purohit-05804a199/)  

