# Tamil Nadu Election Analytics — Power BI

An interactive **Power BI election analytics dashboard** comparing Tamil Nadu Assembly election results between **2021 and 2026**.

The project focuses on constituency-level changes, party performance, regional shifts, winning margins, seat flips, retained seats, and General/SC/ST constituency analysis.

---

## 📊 Project Overview

This project transforms election-result data into an interactive analytical dashboard using **Microsoft Power BI, DAX, and data modeling**.

The dashboard analyzes:

- 2021 vs 2026 seat distribution
- Constituencies that changed hands
- Party-wise gains and losses
- Flip vs Hold seats
- Regional seat distribution
- Winning margins
- Contested and dominant seats
- General, SC, and ST constituencies
- Party performance across regions
- Constituency-level election changes

---

## 🎯 Key Questions Answered

The dashboard answers questions such as:

1. How many constituencies changed hands between 2021 and 2026?
2. Which parties gained the most seats?
3. Which parties lost the most seats?
4. How many seats did each party win in 2021 and 2026?
5. What percentage of constituencies were flipped?
6. Which regions experienced the largest electoral changes?
7. Which constituencies had the narrowest winning margins?
8. Which constituencies had the most dominant wins?
9. How did winning margins change between 2021 and 2026?
10. How many General, SC, and ST seats were flipped?
11. Which parties retained the most seats?
12. Which parties lost the most previously won seats?
13. How is the 2026 Assembly distributed across parties?
14. How does party performance vary by region?

---

## 📌 Key Dashboard KPIs

The main dashboard contains the following KPIs.

### Total Seats

Total number of Assembly constituencies analyzed.

### Seats Flipped

Number of constituencies where the 2021 winner was different from the 2026 winner.

### Flip Rate %

Percentage of constituencies that changed hands.

**Formula:**

> Flip Rate % = Flipped Seats / Total Seats × 100

### Average Win Margin

Average winning margin across the analyzed constituencies.

---

## 🔄 Flip vs Hold Analysis

The core analytical concept of the project is **Flip vs Hold**.

For each constituency:

```text
Winner 2021 = Winner 2026
            ↓
           HOLD



This allows the dashboard to identify:

Seats retained by the 2021 winning party
Seats lost by the 2021 winning party
Parties that gained seats
Parties that lost seats

The analysis can be viewed by:

Party
Region
Reservation category
Constituency
🗳️ Seat Distribution Analysis

The dashboard compares party performance between the two election years.

Seat Distribution Shift: 2021 vs 2026

A comparison of seats won by each party in 2021 and 2026.

This helps identify:

Major seat gains
Major seat losses
Parties retaining their position
Changes in overall political composition
2026 Assembly Composition

A donut chart showing the distribution of 2026 Assembly seats among political parties.

Regional Seat Distribution

A treemap showing 2026 seats across major regions:

South
Central
North
Delta
Kongu
Chennai Metro
🔁 Seats Changed Hands

The project provides a detailed analysis of constituencies that changed hands.

Parties Losing Seats

The party that won the constituency in 2021 but did not win it in 2026.

Parties Gaining Seats

The party that won the constituency in 2026 after a different party had won it in 2021.

The transition is calculated as:

2021 Winner
     ↓
   FLIP
     ↓
2026 Winner

This enables party-to-party seat transition analysis.

🗺️ Regional Analysis

The dashboard divides Tamil Nadu constituencies into regional groups.

Regional analysis includes:

Total seats by region
Party-wise seats by region
2021 regional distribution
2026 regional distribution
Flip vs Hold percentage by region

A 100% stacked bar chart is used to compare the percentage of flipped and retained seats across regions.

📈 Winning Margin Analysis

Winning margins are used to measure electoral competitiveness.

The dashboard compares:

Average Winning Margin — 2021
Average Winning Margin — 2026
Constituency-level margin changes

This helps identify whether constituencies became more competitive or more decisive.

🎯 Winning Margin Categories

Winning margins are grouped into five categories:

Winning Margin	Category
0K – 5K	Very Close
5K – 15K	Moderate
15K – 30K	Comfortable
30K – 50K	Strong
50K+	Landslide

A bar chart shows the number of constituencies falling into each category.

🔍 Contested vs Dominant Seats

The project also identifies seats based on vote share.

Narrow / Contested Seats

Seats where the winning party's vote share is below 35%.

Dominant Wins

Seats where the winning party's vote share is above 50%.

This provides another measure of electoral competitiveness.

🏆 Top Constituency Analysis

The dashboard identifies:

Top 10 Most Contested Seats

Constituencies with the smallest winning margins.

Top 10 Dominant Seats

Constituencies with the largest winning margins.

Win Margin Shift: 2021 vs 2026

A scatter plot compares winning margins between the two election years.

This helps identify constituencies where winning margins:

Increased
Decreased
Remained relatively stable
🧑‍🤝‍🧑 General, SC and ST Analysis

The dashboard also analyzes constituency reservation categories.

The analysis includes:

General seats
SC seats
ST seats
SC seats won by parties
ST seats won by parties
SC seat flips
ST seat flips
Flip vs Hold percentage by reservation category

This allows comparison of electoral changes between:

General vs SC vs ST constituencies

🧮 DAX Analysis

The project uses DAX measures and calculated columns to perform election analysis.

Important Calculated Columns
Winner_2021
Winner_2026
IsFlip
MarginBin
Important Measures
Total Constituencies
Total Flipped Seats
Total Hold Seats
Flip Rate %
Hold Rate %
Average Win Margin 2021
Average Win Margin 2026
Seats Won 2021
Seats Won 2026
Seats Gained
Seats Lost
Dominant Win Seats
Narrow / Contested Seats
SC Seats
ST Seats
SC Flipped Seats
ST Flipped Seats
🗂️ Data Model

The project uses constituency-level election data with supporting tables for party and margin analysis.

constituency_master

The primary constituency-level analytical table.

Important fields include:

AC Number
Constituency
District
Region
Reservation Category
Winner 2021
Winner 2026
Flip / Hold Status
Party_Seat_Summary

Used for party-level seat analysis and visualizations.

Margin Categories

Used to classify winning margins into:

Very Close
Moderate
Comfortable
Strong
Landslide
📊 Power BI Visualizations

The project demonstrates the use of:

KPI Cards
Clustered Bar Charts
Clustered Column Charts
100% Stacked Bar Charts
Donut Charts
Treemaps
Scatter Plots
Tables
Matrix Visuals
Slicers
Interactive Filters
Conditional Formatting
Navigation Buttons
🎨 Dashboard Design

The dashboard uses a professional election-analysis theme.

Main Color Palette
Element	HEX
Dark Navy	#0D1B2A
Gold	#D9B300
Blue	#118DFF
TVK Navy	#12239E
Purple	#744EC2
Orange	#E66C37
Pink	#E044A7
Dark Purple	#6B007B
White	#FFFFFF
Light Gray	#E6E6E6
Text	#252423

The dashboard uses:

Dark navy navigation
White analytical canvas
Gold and blue comparison colors
Consistent party colors
KPI cards
Section dividers
Interactive slicers
Custom navigation buttons

The dashboard is designed using a 16:9 Power BI canvas.

🔄 Analytical Workflow

The overall analytical workflow is:

Raw Election Data
        ↓
Data Cleaning
        ↓
Constituency-Level Data
        ↓
Determine 2021 Winner
        ↓
Determine 2026 Winner
        ↓
Compare Winners
        ↓
Identify FLIP / HOLD
        ↓
Calculate Party-Level Changes
        ↓
Calculate Regional Changes
        ↓
Analyze General / SC / ST Seats
        ↓
Analyze Winning Margins
        ↓
Build DAX Measures
        ↓
Create Power BI Visualizations
        ↓
Interactive Election Dashboard
💡 Key Analytical Concept

The project goes beyond simply displaying election results.

It analyzes electoral change by connecting the results of two election years.

The central relationship is:

2021 Result
     +
2026 Result
     ↓
Seat Transition
     ↓
Flip / Hold
     ↓
Party Gain / Loss
     ↓
Regional Impact
     ↓
Margin & Competitiveness

This makes the project an electoral change and competitiveness analysis dashboard rather than a simple election-result report.

🛠️ Tools & Technologies
Microsoft Power BI
DAX
Power Query
Data Modeling
Data Visualization
GitHub
📁 Repository Structure
TN-Election-Analytics/
│
├── README.md
│
├── PowerBI/
│   └── TN-Election-Analytics.pbix
│
├── Data/
│   ├── tn_2021_results.csv
│   ├── tn_2026_results.csv
│   └── constituency_master.csv
│
├── DAX/
│   ├── seat_analysis.md
│   ├── flip_hold_analysis.md
│   └── margin_analysis.md
│
├── Screenshots/
│   ├── overview.png
│   ├── seats_changed.png
│   ├── margin_analysis.png
│   └── regional_analysis.png
│
└── LICENSE
📷 Dashboard Preview

Add screenshots of the major dashboard pages here.

Election Overview

Seats Changed

Margin Analysis

Regional Analysis

⭐ Project Highlights
234 Assembly Constituencies
163 Constituencies Changed Hands
2021 vs 2026 Party Seat Comparison
Party-wise Flip and Hold Analysis
Regional Electoral Shift Analysis
General / SC / ST Analysis
Winning Margin Classification
Contested vs Dominant Seat Analysis
Constituency-Level Margin Comparison
Interactive Power BI Dashboard
DAX-Based Election Analytics
👨‍💻 Skills Demonstrated

This project demonstrates practical skills in:

Data Analysis
Data Cleaning
Data Modeling
DAX
Power BI
Data Visualization
KPI Development
Comparative Analysis
Regional Analysis
Election Analytics
Dashboard Design
Business Intelligence
📌 Conclusion

This Power BI project provides an interactive view of how the Tamil Nadu Assembly electoral landscape changed between 2021 and 2026.

Instead of focusing only on the final seat count, the dashboard investigates:

Where seats changed hands
Which parties benefited
Which parties lost seats
Which regions experienced the greatest shifts
How competitive individual constituencies were
How patterns differed across General, SC, and ST constituencies

The project demonstrates how raw election data can be transformed into meaningful insights using Power BI, DAX, data modeling, and interactive visualization.


### Important when pasting into GitHub

Copy **only the content inside the outer code block**.

Do **not** copy the first:

```text
```markdown

or the final:


Those are only there to keep the README formatting intact in this chat.

Your GitHub file should start directly with:

```text
# Tamil Nadu Election Analytics — Power BI

and GitHub will automatically render all the headings, tables, bullets, horizontal lines, and images properly.
