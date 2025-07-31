---
layout: page
title: Adventure Works Sales Analysis
description: Excel-based analysis of four years of Adventure Works transactional data
img: assets/img/project5_page.png
importance: 1
category: work
related_publications: false
pretty_table: true
---

{% include figure.liquid loading="eager" max-width="500px" max-height="600px" path="assets/img/project5_ecommerce.png" class="img-fluid rounded z-depth-1" %}
Image from [storyset](https://storyset.com/illustration/ecommerce-web-page/amico)

> **Note**
>
> This project was guided by a tutorial from Ismaila Omeiza M. - Data with Decision [YouTube channel](https://www.youtube.com/watch?v=VxOOt2dP8Jw&ab_channel=DatawithDecision). which provided clear, structured instruction on conducting sales analysis using Excel. The hands-on walkthrough helped deepen my understanding of dashboard design and data storytelling using transactional data
>
> Original Project:
> 
> Title: Data Analysis Project in Excel - Build Interactive Dashboard. Author: Ismaila Omeiza M. - Data with Decision. Platform: [YouTube](https://www.youtube.com/@datalab365).
>
> The original tutorial offered an excellent foundation for building practical data analysis skills. Full credit goes to Data with Decision for the methodology, design approach, and dataset structure. You can explore more of their content on their [YouTube Channel](https://www.youtube.com/@datalab365).
<br/>

## Table Of Contents
- [Executive Summary](#executive-summary)
  - [Primary Goal](#primary-goal)
  - [Solution](#solution)
  - [Key Findings and Recommendations](#key-findings-and-recommendations)
- [Introduction](#introduction)
  - [Business Problem](#business-problem)
  - [Goals](#goals)
- [Methodology](#methodology)
  - [Data Source](#data-source)
  - [Data Overview](#data-overview)
  - [Tools](#tools)
  - [Data Cleaning and Transformation](#data-cleaning-and-transformation)
  - [Data Analysis](#data-analysis)
  - [Data Visualisation](#data-visualisation)
- [Insights](#insights)
  - [Year-over-Year Performance Overview](#year-over-year-performance-overview)
  - [Temporal Trends](#temporal-trends)
  - [Product-Level Insights](#product-level-insights)
  - [Customer Demographics and Geography](#customer-demographics-and-geography)
- [Action Plan](#action-plan)
- [Excel Report](#excel-report)	


## Executive Summary
### Primary Goal
The main goal is to develop a functional and visually engaging Excel dashboard that analyses four years of transactional sales data from Adventure Works. It focuses on refining data interpretation skills, enhancing storytelling through visualisations, and applying structured methodologies for business insight generation. The dashboard is designed to highlight key performance patterns and support data-informed decision-making.


### Solution
This project delivers a comprehensive Excel dashboard tailored for sales data analysis using the Adventure Works dataset. Through a guided methodology, the dashboard offers:
- Visual representations of profit trends across products, regions, and time periods.
- Interactive features that allow users to filter and explore data dynamically.
- Structured insights to support business-oriented decision-making.
- A clear demonstration of analytical thinking and visualisation techniques in Excel.

### Key Findings and Recommendations
<table>
    <thead>
        <tr>
            <th>Finding</th>
            <th>Recommendation</th>
            <th>Plot</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><b>Consistent Growth:</b> Revenue increased steadily, peaking at over $101M in 2007 and 2008.</td>
            <td><b>Analyase factors behind 2007–2008 peaks</b> to inform future revenue strategy.</td>
            <td>{% include figure.liquid loading="eager" path="assets/img/Project5-Revenue2007-2008.png" class="img-fluid rounded z-depth-1" zoomable=true%}</td>
        </tr>
        <tr>
            <td><b>Product Profitability:</b> Premium items (priced above $150), particularly Road-150 Red and Mountain-200, consistently drove high profits.</td>
            <td><b>Refine product strategy by prioritising premium, high-margin items</b> such as Road-150 Red and Mountain-200. <br>
Consider rationalising the SKU portfolio to eliminate low-profit contributors and enhance overall profitability </td>
            <td>{% include figure.liquid loading="eager" path="assets/img/Project5-Product-Profitability.png" class="img-fluid rounded z-depth-1" zoomable=true%}</td>
        </tr>
        <tr>
            <td><b>Seasonal Peaks:</b> Profit concentration occurred mid-year (May–June) and year-end (October–December), varying by year.</td>
            <td rowspan=2><b>Optimise campaign scheduling</b> by aligning marketing efforts with observed profitability peaks — mid-year (May–June), year-end (October–December), and high-performing weekdays, particularly Thursdays. <br>
This timing strategy enhances impact and revenue potential. </td>
            <td>{% include figure.liquid loading="eager" path="assets/img/Project5-Seasonal-Peaks.png" class="img-fluid rounded z-depth-1" zoomable=true%}</td>
        </tr>
        <tr>
            <td><b>Weekday Advantage:</b> Weekdays contributed more than 70% of profit across all four years, with Thursday ranking in the top 3 every year. </td>
          <td>{% include figure.liquid loading="eager" path="assets/img/Project5-Weekday.png" class="img-fluid rounded z-depth-1" zoomable=true%}</td>
        </tr>
        <tr>
            <td> <b>Customer Drivers:</b> The 50+ age group generated nearly half of total customer profit, and gender impact was nearly balanced.</td>
            <td><b>Enhance Customer Segmentation:</b> Target older customers with tailored promotions and loyalty benefits. <br>
Given gender neutrality in profit distribution, campaigns can focus on shared value drivers rather than gender-specific messaging. </td>
            <td>{% include figure.liquid loading="eager" path="assets/img/Project5-age_group.png" class="img-fluid rounded z-depth-1" zoomable=true%}</td>
        </tr>
        <tr> 
            <td><b>Geographic Focus:</b> Australia and the United States accounted for over 60% of total profit.</td>
            <td><b>Strengthen regional strategy</b> by expanding investments in high-performing markets such as Australia and the United States, which collectively account for over 60% of total profit. <br>
Focused efforts in these regions can amplify revenue growth and market share. </td>
            <td><a href="assets/img/Projct5-au-usa.png" target="_blank"><img src="assets/img/Projct5-au-usa.png" class="img-fluid rounded z-depth-1" style="cursor: zoom-in;"></a></td>
        </tr>
    </tbody>
</table>


## Introduction
### Business Problem
Adventure Works, a multinational retail company, manages a diverse product portfolio across several global regions. However, the organisation faces challenges in identifying key profit drivers and regional performance disparities over time. Without a cohesive and accessible method for analysing historical sales data, stakeholders struggle to make informed decisions regarding product strategy, regional investment, and seasonal demand planning. This project addresses the need for a visually intuitive dashboard that consolidates four years of transactional data, enabling clearer insight into sales trends and unlocking opportunities for data-driven decision-making.

### Goals
- Summarise Multi-Year Sales Performance: Present a high-level overview of Adventure Works' sales trends over a four-year period to help users quickly grasp historical performance.
- Highlight Profit Drivers by Category and Region: Identify which product categories and geographical markets contributed most significantly to revenue generation.
- Enable Dynamic Data Exploration: Integrate interactive Excel features (e.g. slicers, filters) to allow users to customise views and explore specific timeframes, regions, or product groups.
- Reveal Seasonal and Temporal Patterns: Analyse time-based trends to uncover seasonal spikes or declines in sales, guiding future planning and promotional activities.
- Support Strategic Decision-Making: Provide actionable insights through visualisations that help stakeholders evaluate investment, inventory, and marketing strategies.
- Create a Visually Intuitive Dashboard Experience: Ensure the layout is clean, coherent, and easily navigable—making the dashboard approachable for users with varying data literacy levels.

## Methodology
### Data source
The dataset used in this project was provided as part of a tutorial from the Data with Decision [YouTube channel](https://www.youtube.com/watch?v=VxOOt2dP8Jw&ab_channel=DatawithDecision). It features transactional sales records from the fictional company Adventure Works, commonly employed in training scenarios for data analysis and dashboard development. All data was made available for educational purposes and aligns with the instructional content presented in the original video.

### Data Overview
The project utilises the [AdventureWorks.xlsx](https://github.com/alejandralopezgalan/alejandralopezgalan.github.io/blob/master/assets/data/Project5_AdventureWorks_Database.xlsx) workbook, which contains six relational tables:
- `FactInternetSales`: The central fact table housing over 60,000 rows of transactional records, linked to other tables through keys such as `ProductKey`, `CustomerKey`, `SalesTerritoryKey`, and date fields. It stores detailed sales metrics including quantities, discounts, costs, and revenue values. 
- `DimCustomer`: Provides detailed customer demographics and contact attributes, comprising 18,484 individual records. This dimension links to the fact table via CustomerKey, and includes variables such as full name, birth date, marital status, income level, multilingual education and occupation details, geographical location, purchase history, and commuting distance. It enriches the sales model with personal and regional context for more targeted analysis.
- `DimDate`: A dedicated calendar dimension comprising 1,461 date records. It supports time-based analysis by providing structured fields such as full date values, day and month names in multiple languages (English, Spanish, French), and hierarchical attributes for calendar and fiscal periods.
- `DimProduct`: Contains 606 records detailing product-level attributes used for sales analysis. This table is linked to the central fact table via ProductKey, and includes fields for product category, colour, size, cost, list pricing, manufacturing specifics, and availability dates. It also features multilingual product descriptions, supporting accessibility and localisation across global markets.
- `DimGeography`: Consists of 655 records offering geographical context for customer data. This dimension includes city, state or province, postal code, and country fields, along with regional identifiers that support location-based analysis. Country names are provided in English, Spanish, and French, enabling multilingual reporting and global segmentation. 
- `DimSalesTerritory`: Comprises 10 records that provide a higher-level classification of global sales regions. This dimension includes fields for territory name, country grouping, and territory image identifiers. It enables segmentation and comparative analysis across broader geographical markets, supporting strategic insight into regional performance.

All tables form an integrated data model that enables robust cross-dimensional analysis. The dataset is fictional and provided exclusively for educational purposes, aligning with the structure and learning goals outlined in the original YouTube tutorial and this project. It serves as a practical foundation for developing analytical capabilities, data visualisation skills, and professional dashboard design in a simulated business context.

### Tools
- Microsoft Excel: Utilised for exploring, cleaning, transforming, and visualising the data through an interactive dashboard. The project also incorporates Power Query to load and shape multiple relational tables efficiently, forming the foundation of the data model.

### Data Cleaning and Transformation
Power Query was used to load the six relational tables from the AdventureWorks workbook, establish connections, create new measures, and select only the columns relevant to the dashboard analysis. 

#### FactInternetSales
 Performance insights were developed using the following variables from the `FactInternetSales` dataset:
`ProductKey`, `OrderDateKey`, `DueDateKey`, `ShipDateKey`, `CustomerKey`, `SalesTerritoryKey`, `OrderQuantity`, `UnitPrice`, `ProductStandardCost` (renamed as `Cost`), and `OrderDate`.

Several calculated fields were added to enrich the dataset:
- `TotalRevenue`: Defined as `OrderQuantity * UnitPrice`, this measure was used to calculate gross sales revenue. It was formatted as a Currency-type variable.
- Cost of Goods Sold (`COGS`): Calculated using `OrderQuantity * Cost`, this metric estimates product-level expenditure. It was also formatted as a Currency-type variable.
- `TotalProfit`: Estimated with the formula `TotalRevenue – COGS`, representing net profit per transaction. This field was formatted as Currency.
- `Product Price Type`: A conditional text field categorising products based on unit price, if UnitPrice ≤ 150 then "Less Expensive", else "Expensive". It was formatted as a Text-type variable to enable segmentation.

#### DimCustomer
The following columns were retained from the `DimCustomer` table to support performance analysis: 
`CustomerKey`,	`GeographyKey`,	`CustomerAlternateKey`,	`BirthDate`,	and `Gender`.

Additional fields were introduced to enhance segmentation and demographic insights:
- `Full Name`: Created by combining the `FirstName` and `LastName` fields into a single text variable.
- `Customer Age`: Derived using a Power Query formula to calculate the customer’s age based on their `BirthDate`.

``` 
= Table.AddColumn(#"Choose Column", "Customer Age", each 
  let 
    source = #date[BirthDate],
    Today = Date.From(DateTime.LocalNow()),
    Age = Duration.From(Today - [BirthDate]),
    Years = Duration.From(Duration.From(Age) / #duration(365,0,0,0)) 
  in 
    Years)
```

- `Age Group`: A conditional Text-type variable categorising customers into age bands using the following logic:
  
``` 
= Table.AddColumn(#"Changed Type1", "Age Group", each 
  if [Customer Age] <= 24 then "0–24" 
  else if [Customer Age] <= 29 then "25–29" 
  else if [Customer Age] <= 34 then "30–34" 
  else if [Customer Age] <= 39 then "35–39" 
  else if [Customer Age] <= 44 then "40–44" 
  else if [Customer Age] <= 49 then "45–49" 
  else "50 Plus")
```

#### DimDate
From the `DimDate` table only the `FullDateAlternateKey` field was included, and renamed as `Date`.  to simplify the time-based analysis. 

Several calculated columns were generated to support trend exploration, period segmentation, and dashboard filtering:
- `Year`: Extracted using Year([Date]) and formatted as an Integer-type variable. Only data from 2011 onward was included, excluding 2009 and 2010 from the analysis.
- `Month Number`: Derived using Date.Month([Date]) to support chronological sorting, formatted as Integer.
- `Month Name`: Created with Date.MonthName([Date]) and truncated to the first three characters (e.g. Jan, Feb, Mar), formatted as Text-type.
- `Day Name`: Obtained via Date.DayOfWeekName([Date]) and shortened to three-letter labels (e.g. Mon, Tue, Wed), formatted as Text.
- `WeekTypes`: A conditional text column categorising the day as either Weekend or Weekday:
  
```
if [Day Name] = "Sun" then "Weekend"
else if [Day Name] = "Sat" then "Weekend"
else "Weekday"
```

- `Quarter`: Generated using Date.QuarterOfYear([Date]), formatted as Integer with a prefix to display in dashboard visuals as Qtr-1, Qtr-2, Qtr-3, or Qtr-4.
- `DayNumber`: Extracted using Date.DayOfWeek([Date]), formatted as Integer to support ordering of weekdays in charts and slicers.


#### DimProduct
The analysis incorporated these columns from the `DimProduct` dataset:
- `ProductKey`
- `EnglishProductName` (renamed as `ProductName`).
- `Color`

Missing values in the `Color` column were replaced with the label `Unspecified` to ensure consistency in product categorisation and visual filtering.

#### DimGeography
Key geographical fields were extracted from `DimGeography` to enable location-based insights:
- `City` – Provides local-level geographical context.
- `EnglishCountryRegionName` – Renamed as `Country` for clarity and consistency.
- `SalesTerritoryKey` – Enabled connection to higher-level territorial classification.

#### DimSalesTerritory
The following fields were retained from the `DimSalesTerritory` table to support regional analysis:
`SalesTerritoryKey`,	`SalesTerritoryAlternateKey`,	`SalesTerritoryRegion`,	`SalesTerritoryCountry`,	and `SalesTerritoryGroup`. 

All entries containing `NA` values were excluded to ensure consistency and accuracy in territorial segmentation.

### Data Analysis
Pivot tables were used to uncover sales performance patterns, customer segmentation insights, and product profitability across regions and time periods. All pivot tables, calculations, and dashboards are available in the [Adventure_Works_Sales_Analysis.xlsm](https://github.com/alejandralopezgalan/alejandralopezgalan.github.io/blob/master/assets/data/Project5_Adventure_Works_Sales_Analysis.xlsm) file within the repository.

#### Pivot Table Sheets

##### Pivot_ProfitByYear
This sheet presents a concise year-over-year analysis of Adventure Works sales data from 2005 to 2008, based on key financial and transactional metrics. 
- Steady Growth: Revenue rose from $33.37M in 2005 to over $101M in both 2007 and 2008, with corresponding increases in transactions and order quantities.
- Profitability: Profit margins remained consistently above 40%, with Total Profit peaking in 2007 at $42.55M and holding strong in 2008 at $42.16M.
- Transaction Volume: Transaction counts surged from 1.01K in 2005 to 32.27K by 2008, illustrating significant operational scale-up.
- Product Dynamics (2005 snapshot): Of 606 products, only 25 remained unsold, implying an almost complete sales conversion.
- Above-Average Profit Analysis: In 2007 and 2008, profits exceeded the calculated four-year average (~$31.57M), contributing a combined $84.7M or 67.1% of total profit during the period.

##### Pivot_ProfitByMonth-Day-Qtr
This sheet presents a time-based breakdown of Total Profit for a selected year, offering insight into seasonal, weekly, and daily performance patterns. While results vary depending on the year chosen, the following summary reflects trends observed for 2006.
- Top-performing months: May ($3.09M), March ($2.87M), and June ($2.83M) collectively contributed 47.5% of annual profit, indicating a strong mid-year surge.
- Seasonal Dips: November ($1.42M) and September ($1.59M) returned the lowest monthly profits, suggesting potential seasonal slowdowns.
- Quarterly Breakdown: Q2 led the year with $8.65M (31% of total profit), followed by Q1 ($7.76M). Profit tapered slightly in Q3 ($6.02M) and Q4 ($5.74M), reinforcing mid-year peak performance.
- Day-of-Week Trends: Monday ($4.43M), Sunday ($4.12M), and Friday ($4.21M) were the top contributors, accounting for 45.2% of annual profit. Wednesday and Thursday showed comparatively lower results.
- Weekday vs Weekend Split: Weekdays generated 71.91% of total profit ($20.26M), while weekends represented 28.09% ($7.91M). Despite the volume difference, margin consistency suggests that weekend transactions remained equally profitable.

##### Pivot_Product_Analysis
This sheet offers a deep dive into product-level profitability, highlighting which items contributed most to overall profit during the analysed period. Trends may shift annually; however, this overview focuses on data observed during 2006.
- Top-Performing Products: Five variants of Road-150 Red (sizes 44–62) emerged as the leading contributors, generating a combined $12.38M in total profit.
- High Sales Conversion: The Top 5 Products alone delivered over $12M in profit, representing a significant portion of total earnings. These products also dominated both quantity sold and frequency of transactions, indicating high demand and strong market placement.
- Colour & Price Segmentation: Products were grouped by colour category (e.g. Red, Black, Silver) and by price type (Less Expensive vs Expensive) to uncover purchasing behaviour. Red-coloured products were consistently high performers across both profit and quantity metrics.

##### Pivot_Customers_Analysis
This sheet delivers a comprehensive customer profitability analysis, integrating demographic, transactional, and geographic insights. Here’s a concise breakdown for 2006:
- Top Customers: The five highest-earning customers contributed a combined $1.38M in profit, underscoring the value of targeted relationship strategies.
- Customer Demographics:
  - Total Customers: 2,577.
  - Average Age: 46 years.
  - Gender Split: Female with $14.48M in profit, Male with $13.97M in profit. Gender contribution is balanced, with a slight edge in profit generation from female customers.
  - Age Group Performance: 50 Plus dominates with $11.51M, contributing over 48% of total customer profit.
- Geographic Distribution: Top Countries were Australia ($9.9M) and United States: ($9.0M). United Kingdom, Canada, Germany, and France followed with $2.2M–$2.7M each.

### Data Visualisation
The results were visualised in two dashboards.

#### Sales Performance & Time-Based Insights
This interactive dashboard showcases key performance metrics and temporal trends for Adventure Works sales data. It includes filters and visuals that enable users to explore transactional and profitability patterns by date, country, weekday, and quarter.
The following screenshot display the results of the analysis on the year 2006. 

Key Components:
- Header Navigation 
Includes buttons for switching between dashboard views (Time Series, Products & Customers) and resetting filters.

- Summary KPIs
Displays core metrics such as:
  - Order Quantity: 28.41K (+46.41% compared to the preious year, 2005).
  - Total Revenue: $69.48M.
  - Total Profit: $28.18M.
  - Transactions: 2.68K (+45.09% compared to the preious year, 2005).
  - Profit Margin: 40.6%.
  - Total COGS: $41.31M.

- Yearly Profit Comparison: A horizontal bar chart comparing total profit across four years, with 2007 and and 2008 contributing the highest share (67.1%). In this graph it is also possible to select the Revenue or Number of Transacions to be displayed.
- Monthly Profit Trends (2006): A line graph reveals seasonal patterns in profitability, with peaks in May, March, and June, representing 47.5% of the year's profit.
- Weekday Profit Breakdown: A vertical bar chart shows profit distribution by day of the week, with Monday, Friday, and Sunday emerging as top contributors.
- Weekday vs Weekend Analysis: A donut chart indicates that weekdays generated 71.91% of total profit, with weekends accounting for the remaining 28.09%.
- Quarterly Performance Summary: Each quarter is displayed with its respective contribution, led by Q2 ($8.65M) followed by Q1 ($7.76M).

{% include figure.liquid loading="eager" path="assets/img/project5_Sales_Performance.png" class="img-fluid rounded z-depth-1" %}

#### Product & Customer-Level Profitability 
This dashboard presents detailed profitability insights across products, customers, and demographic segments for Adventure Works, with results filtered by year. It enables exploration of how individual items and customer groups contribute to overall financial performance.

Key Components:
- Top 5 Profitable Products: Road-150 Red (sizes 44–62) dominates, contributing $12.38M collectively, or 43.9% of total profit.
- Product Summary: Out of 606 available products, only 56 were sold, highlighting an opportunity for inventory optimisation.
- Profit by Product Colour: 
  - Red: $16.36M.
  - Black: $7.86M.
  - Silver: $3.39M.
  - Other colours returned no profit, indicating limited customer preference.
- Price Category Breakdown: Products generating profit were exclusively priced above $150, reflecting a high-value portfolio.
- Top 5 Customers: Each contributed around $29.76K, totalling 0.5% of overall profit, suggesting a wide and evenly distributed customer base.
- Customer Demographics:
  - Total customers: 2,677.
  - Average age: 46.
  - 50 Plus age group: $11.51M (40.8% of profit), showing strong purchasing power in older demographics.
- Gender-Based Profit Contribution: A near-even split, with a slight edge toward female customer profitability.
  - Female: 51.4%.
  - Male: 48.6%.
- Geographic Trends: Supported by map visuals highlighting spatial distribution.
  - Australia & United States: Combined contribution of 65.8% of total profit.
- Year Filter: Allows users to switch between 2005–2008 to compare trends across time.
- Country Filter: Enables focused analysis by geographic region.

{% include figure.liquid loading="eager" path="assets/img/project5_Product_Customer-Profitability.png" class="img-fluid rounded z-depth-1" %}

## Insights
### Year-over-Year Performance Overview
- Revenue growth: Increased from $33.37M in 2005 to over $101M in 2007 and 2008, reflecting consistent business expansion.
- Profit peaks: 2007 delivered the highest annual profit ($42.55M), followed closely by 2008 ($42.16M). These two years contributed 67.1% of total profit across the four-year span.
- Operational scale-up: Total transactions rose from 1.01K in 2005 to 32.27K by 2008, demonstrating significant growth in sales activity.
- Product conversion success: In 2005, only 25 of 606 products were sold (4.1%). By 2008, the number of sold products quadrupled, with many proving highly profitable.

### Temporal Trends
- Top months by year:
  - 2005 & 2007: December, November, October.
  - 2006: May, March, June (47.5% of that year’s profit).
  - 2008: June, May, April.
- Weekday dominance: - Weekdays consistently contributed over 70% of total profit across all four years. Thursday ranked among the top three most profitable days throughout the entire period.
- Most profitable quarters:
  - Q4 in 2005 ($7.41M).
  - Q2 in 2006 ($8.65M).
  - Q4 in 2007 ($17.63M).
  - Q1 in 2008 ($18.44M).

### Product-Level Insights
- High-margin strategy: All profitable items were priced above $150, underscoring the effectiveness of premium product positioning.
- Product concentration: Road-150 Red and Mountain-200 variants each accounted for at least 31% of annual profit, peaking in 2005 with over 75% of that year’s profit.
- Colour segmentation: Red products were top performers in 2005 and 2006, while black variants led in 2007 and 2008.
- Inventory scope: Sold products ranged from 25 in 2005 to 102 in 2008, suggesting opportunities for SKU optimisation and targeted product marketing.

### Customer Demographics and Geography
- Age-based profitability: Customers aged 50+ generated at least 39% of total profit during the analysed period.
- Gender contribution: Profit was nearly evenly split between male and female customers, with a slight edge toward female profitability.
- Geographic distribution: Australia and the United States consistently ranked as the top-performing regions, contributing over 60% of total customer profit.
- Top customers: Each of the five highest-value customers generated at least $29K in profit. 


## Action Plan
1. Refine Product Portfolio
  - Prioritise high-performing items like Road-150 Red and Mountain-200, which consistently drive yearly profit.
  - Eliminate or rebrand low-selling SKUs, and focus on items priced above $150 to sustain profit margins.

2. Optimise Marketing Timing
  - Launch campaigns during peak months (e.g. May–June, October–December) based on year-specific trends.
  - Target Mondays and Thursdays for promotions, leveraging weekday profitability (>70%).

3. Target Key Demographics
  - Develop tailored messaging for 50+ age group, which contributed nearly 50% of total profit.
  - Maintain inclusive targeting across genders, given their near-equal financial impact.

4. Strengthen Geographic Presence
  - Invest in regional campaigns for Australia and the United States, which generated over 60% of total customer profit.

5. Cultivate Top Customer Relationships
  - Introduce loyalty benefits or premium tiers for top spenders, each generating ~$29K in individual profit.

## Excel Report
To explore the full analysis and dashboards, access the Excel file via the following [link](https://github.com/alejandralopezgalan/alejandralopezgalan.github.io/blob/master/assets/data/Project5_Adventure_Works_Sales_Analysis.xlsm). The workbook is organised into two main sections:
- Pivot Analysis Sheets
The first four tabs, Pivot_ProfitByYear, Pivot_ProfitByMonth-Day-Qtr, Pivot_Product_Analysis, and Pivot_Customers_Analysis, contain the underlying pivot tables and detailed analytical breakdowns.
- Dashboard Visuals
The final two sheets, Time_Series_Dashboard and Products_Customer_Dashboard, feature interactive dashboards with curated plots that illustrate key performance insights across time, product categories, and customer demographics.

{% include figure.liquid loading="eager" path="assets/video/project5_gif.gif" class="img-fluid rounded z-depth-1" %}


