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
- **Interactive Power BI Dashboard** with dynamic filters and visualizations.  
- **Role-Specific Player Evaluation** using predefined performance thresholds.  
- **Real-Time Projections** for team scoring/defending capabilities.  
- **Drag-and-Drop Team Builder** to assemble the final 11.  
- **Custom Alerts** for underperforming players.  

---

## 🚀 Steps to Build the Project  
1. **Data Collection**:  
   - Web-scraped raw T20 data using Python scripts.  
   - Stored data in JSON format.  
2. **Preprocessing**:  
   - Converted JSON to CSV and cleaned data using Pandas/Power Query.  
   - Applied SQL for filtering and aggregation.  
3. **Dashboard Development**:  
   - Built interactive visuals in Power BI (charts, matrices, heatmaps).  
   - Integrated DAX formulas for dynamic metrics.  
4. **Team Selection**:  
   - Shortlisted top players using role-specific criteria.  
   - Curated a balanced squad using the Team Builder panel.  

---


---

## 🛠️ Technologies Used  
- **Data Collection**: Python (BeautifulSoup, Requests)  
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

## 📈 Dashboard Features  
- **Interactive Visualizations**:  
  - Scatter plots (Strike Rate vs. Economy).  
  - Radar charts for bowler performance.  
  - Heatmaps for boundary and dot ball analysis.  
- **Dynamic Filters**:  
  - Filter by team, role, tournament stage, or venue.  
- **Team Builder**:  
  - Drag-and-drop interface to assemble the final 11.  
  - Auto-calculates projected team averages.  

---

## 🔑 Key DAX Queries  
### Batting Metrics  
```dax
Total Runs = SUM(fact_batting_summary[runs])  
Strike Rate = DIVIDE([Total Runs], [Total Balls Faced], 0) * 100  
Boundary % = DIVIDE(SUM(fact_batting_summary[Boundary runs]), [Total Runs], 0)


This README provides a structured, detailed guide to your project. Adjust links, filenames, and sections to match your repository! 🏆

🔗 Connect
GitHub | LinkedIn 

