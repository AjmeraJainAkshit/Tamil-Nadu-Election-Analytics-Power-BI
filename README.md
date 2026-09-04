# Tamil Nadu Election Analytics — Power BI

An interactive **Power BI election analytics dashboard** comparing Tamil Nadu Assembly election results between **2021 and 2026**.

The project focuses on constituency-level changes, party performance, regional shifts, winning margins, seat flips, retained seats, and General/SC/ST constituency analysis.

---

## 📊 Project Overview

This project transforms constituency-level election data into an interactive analytical dashboard using **Microsoft Power BI, DAX, Power Query, and data modeling**.

The dashboard analyzes:

- 2021 vs 2026 seat distribution
- Constituencies that changed hands
- Party-wise gains and losses
- Flip vs Hold seats
- Regional electoral shifts
- Winning margins
- Contested and dominant seats
- General, SC, and ST constituencies
- Party performance across regions
- Constituency-level election changes

---

## 🎯 Key Questions Answered

The dashboard answers important questions such as:

- How many constituencies changed hands between 2021 and 2026?
- Which parties gained the most seats?
- Which parties lost the most seats?
- How many seats did each party win in 2021 and 2026?
- What percentage of constituencies were flipped?
- Which regions experienced the largest electoral changes?
- Which constituencies had the narrowest winning margins?
- Which constituencies had the most dominant wins?
- How did winning margins change between 2021 and 2026?
- How many General, SC, and ST seats were flipped?
- Which parties retained the most seats?
- Which parties lost the most previously won seats?
- How is the 2026 Assembly distributed across parties?
- How does party performance vary by region?

---

## 📌 Key Dashboard KPIs

The dashboard contains several key performance indicators.

### Total Constituencies

Total number of Assembly constituencies analyzed in the dashboard.

### Total Flipped Seats

Number of constituencies where the 2021 winning party was different from the 2026 winning party.

### Flip Rate %

Percentage of constituencies that changed hands between 2021 and 2026.

```text
Flip Rate % = Total Flipped Seats / Total Constituencies × 100
```

### Total Hold Seats

Number of constituencies where the 2021 winning party also won the constituency in 2026.

### Hold Rate %

Percentage of constituencies retained by the 2021 winning party.

```text
Hold Rate % = Total Hold Seats / Total Constituencies × 100
```

### Average Win Margin

Average winning margin across the analyzed constituencies.

The dashboard compares the average winning margin between **2021 and 2026** to understand changes in electoral competitiveness.

---

## 🔄 Flip vs Hold Analysis

The core analytical concept of the project is **Flip vs Hold**.

For each constituency, the 2021 winner is compared with the 2026 winner.

### Hold

If the same party wins the constituency in both elections:

```text
2021 Winner
     ↓
   HOLD
     ↓
2026 Winner
```

### Flip

If a different party wins the constituency in 2026:

```text
2021 Winner
     ↓
   FLIP
     ↓
2026 Winner
```

This allows the dashboard to identify:

- Seats retained by the 2021 winning party
- Seats lost by the 2021 winning party
- Parties that gained seats
- Parties that lost seats

The analysis can be viewed by:

- Party
- Region
- Reservation category
- Constituency

---

## 🗳️ Seat Distribution Analysis

The dashboard compares party performance between the two election years.

### Seat Distribution Shift: 2021 vs 2026

A comparison of seats won by each party in 2021 and 2026.

This helps identify:

- Major seat gains
- Major seat losses
- Parties retaining their position
- Changes in overall political composition

### 2026 Assembly Composition

A donut chart showing the distribution of 2026 Assembly seats among political parties.

### Regional Seat Distribution

A treemap showing 2026 seats across major regions:

- South
- Central
- North
- Delta
- Kongu
- Chennai Metro

---

## 🔁 Seats Changed Hands

The project provides a detailed analysis of constituencies that changed hands between 2021 and 2026.

### Parties Losing Seats

The party that won the constituency in 2021 but did not win it in 2026.

### Parties Gaining Seats

The party that won the constituency in 2026 after a different party had won it in 2021.

The transition can be represented as:

```text
2021 Winner
     ↓
   FLIP
     ↓
2026 Winner
```

For example:

```text
Party A
   ↓
 FLIP
   ↓
Party B
```

This represents a constituency where **Party A won in 2021** and **Party B won in 2026**.

This enables party-to-party seat transition analysis.

---

## 🗺️ Regional Analysis

The dashboard divides Tamil Nadu constituencies into regional groups.

The regions analyzed include:

- South
- Central
- North
- Delta
- Kongu
- Chennai Metro

Regional analysis includes:

- Total seats by region
- Party-wise seats by region
- 2021 regional distribution
- 2026 regional distribution
- Flip vs Hold percentage by region

A **100% stacked bar chart** is used to compare the percentage of flipped and retained seats across regions.

This helps identify which regions experienced greater electoral changes.

---

## 📈 Winning Margin Analysis

Winning margins are used to measure electoral competitiveness.

The dashboard compares:

- Average Winning Margin — 2021
- Average Winning Margin — 2026
- Constituency-level margin changes

This helps identify whether constituencies became:

- More competitive
- Less competitive
- More decisive
- Relatively stable

The dashboard also provides constituency-level comparisons of winning margins between the two election years.

---

## 🎯 Winning Margin Categories

Winning margins are grouped into five categories.

| Winning Margin | Category |
|---|---|
| 0K – 5K | Very Close |
| 5K – 15K | Moderate |
| 15K – 30K | Comfortable |
| 30K – 50K | Strong |
| 50K+ | Landslide |

A bar chart shows the number of constituencies falling into each winning-margin category.

This classification helps identify the overall competitiveness of the election.

---

## 🔍 Contested vs Dominant Seats

The project also identifies seats based on the winning party's vote share.

### Narrow / Contested Seats

Seats where the winning party's vote share is below **35%**.

These seats can indicate relatively competitive electoral contests.

### Dominant Wins

Seats where the winning party's vote share is above **50%**.

These seats indicate stronger electoral dominance.

This provides another measure of electoral competitiveness in addition to winning margin.

---

## 🏆 Top Constituency Analysis

The dashboard identifies the most competitive and decisive constituencies.

### Top 10 Most Contested Seats

Constituencies with the smallest winning margins.

These constituencies represent the closest electoral contests.

### Top 10 Dominant Seats

Constituencies with the largest winning margins.

These constituencies represent the most decisive wins.

### Win Margin Shift: 2021 vs 2026

A scatter plot compares winning margins between the two election years.

This helps identify constituencies where winning margins:

- Increased
- Decreased
- Remained relatively stable

---

## 🧑‍🤝‍🧑 General, SC and ST Analysis

The dashboard also analyzes constituency reservation categories.

The analysis includes:

- General seats
- SC seats
- ST seats
- SC seats won by parties
- ST seats won by parties
- SC seat flips
- ST seat flips
- Flip vs Hold percentage by reservation category

This allows comparison of electoral changes between:

**General vs SC vs ST constituencies**

The analysis helps understand whether electoral changes differed across reservation categories.

---

## 🧮 DAX Analysis

The project uses **DAX measures and calculated columns** to perform election analysis.

### Important Calculated Columns

- `Winner_2021`
- `Winner_2026`
- `IsFlip`
- `MarginBin`

### Important Measures

- `Total Constituency`
- `Total Flipped`
- `Total Hold`
- `Flip Seat %`
- `Hold Seat %`
- `Avg Win Margin 2021`
- `Avg Win Margin 2026`
- `Seats Won 2021`
- `Seats Won 2026`
- `Seats Gained in 2026`
- `Seats Lost in 2026`
- `Dominant Win Seats 2026`
- `Narrow Contested Seats 2026`
- `SC Seats 2026`
- `ST Seats 2026`
- `SC Seats 2026 won by DMK`
- `ST Flipped`

---

## 🗂️ Data Model

The project uses constituency-level election data with supporting tables for party and margin analysis.

### `constituency_master`

The primary constituency-level analytical table.

Important fields include:

- AC Number
- Constituency
- District
- Region
- Reservation Category
- Winner 2021
- Winner 2026
- Flip / Hold Status

### `Party_Seat_Summary`

A supporting table used for party-level seat analysis and visualizations.

### `Margin Categories`

A supporting table used to classify winning margins into five categories:

- Very Close
- Moderate
- Comfortable
- Strong
- Landslide

---

## 📊 Power BI Visualizations

The project demonstrates the use of multiple Power BI visualizations.

### Main Visuals

- KPI Cards
- Clustered Bar Charts
- Clustered Column Charts
- 100% Stacked Bar Charts
- Donut Charts
- Treemaps
- Scatter Plots
- Tables
- Matrix Visuals
- Slicers
- Interactive Filters
- Conditional Formatting
- Navigation Buttons

These visualizations allow users to explore election results at both summary and constituency levels.

---

## 🎨 Dashboard Design

The dashboard uses a professional election-analysis theme.

### Main Color Palette

| Element | HEX |
|---|---|
| Dark Navy | `#0D1B2A` |
| Gold | `#D9B300` |
| Blue | `#118DFF` |
| TVK Navy | `#12239E` |
| Purple | `#744EC2` |
| Orange | `#E66C37` |
| Pink | `#E044A7` |
| Dark Purple | `#6B007B` |
| White | `#FFFFFF` |
| Light Gray | `#E6E6E6` |
| Text | `#252423` |

The dashboard uses:

- Dark navy navigation
- White analytical canvas
- Gold and blue comparison colors
- Consistent party colors
- KPI cards
- Section dividers
- Interactive slicers
- Custom navigation buttons

The dashboard is designed using a **16:9 Power BI canvas**.

---

## 🔄 Analytical Workflow

The overall analytical workflow is:

```text
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
```

---

## 💡 Key Analytical Concept

The project goes beyond simply displaying election results.

It analyzes **electoral change** by connecting the results of two election years.

The central relationship is:

```text
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
```

This makes the project an **electoral change and competitiveness analysis dashboard** rather than a simple election-result report.

---

## 🛠️ Tools & Technologies

The project was developed using:

- **Microsoft Power BI**
- **DAX**
- **Power Query**
- **Data Modeling**
- **Data Visualization**
- **GitHub**

---

## 📁 Repository Structure

```text
Tamil-Nadu-Election-Analytics-Power-BI/
│
├── README.md
│
├── TN Elections.pbix
│
├── Screenshots/
│   ├── overview.png
│   ├── seats_changed.png
│   ├── margin_analysis.png
│   └── regional_analysis.png
│
└── LICENSE
```

---

## 📷 Dashboard Preview

The Power BI dashboard contains multiple analytical pages covering election overview, seat changes, winning margins, regional analysis, and reservation-category analysis.

### Election Overview

![Election Overview](Screenshots/overview.png)

### Seats Changed

![Seats Changed](Screenshots/seats_changed.png)

### Margin Analysis

![Margin Analysis](Screenshots/margin_analysis.png)

### Regional Analysis

![Regional Analysis](Screenshots/regional_analysis.png)

---

## ⭐ Project Highlights

- **234 Assembly Constituencies**
- **163 Constituencies Changed Hands**
- 2021 vs 2026 Party Seat Comparison
- Party-wise Flip and Hold Analysis
- Regional Electoral Shift Analysis
- General / SC / ST Analysis
- Winning Margin Classification
- Contested vs Dominant Seat Analysis
- Constituency-Level Margin Comparison
- Interactive Power BI Dashboard
- DAX-Based Election Analytics

---

## 👨‍💻 Skills Demonstrated

This project demonstrates practical skills in:

- Data Analysis
- Data Cleaning
- Data Modeling
- DAX
- Power BI
- Data Visualization
- KPI Development
- Comparative Analysis
- Regional Analysis
- Election Analytics
- Dashboard Design
- Business Intelligence

---

## 📌 Conclusion

This Power BI project provides an interactive view of how the Tamil Nadu Assembly electoral landscape changed between **2021 and 2026**.

Instead of focusing only on the final seat count, the dashboard investigates:

- Where seats changed hands
- Which parties benefited
- Which parties lost seats
- Which regions experienced the greatest shifts
- How competitive individual constituencies were
- How winning margins changed
- How patterns differed across General, SC, and ST constituencies

The project demonstrates how election data can be transformed into meaningful insights using:

**Power BI + DAX + Power Query + Data Modeling + Interactive Visualization**

Overall, the project is designed as an **electoral change and competitiveness analysis dashboard** that provides a constituency-level view of political shifts between two election years.

---

## 📜 Disclaimer

This repository is intended for **data analysis and visualization purposes**.

The dashboard presents analytical comparisons based on the data used in the project. It should not be interpreted as political advice, prediction, or endorsement of any political party or candidate.
