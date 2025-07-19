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
  - [Key Findings](#key-findings)
  - [Recommendations](#recommendations)
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

### Key Findings
- Consistent Growth: Revenue increased steadily, peaking at over $101M in 2007 and 2008.
- Product Profitability: Premium items (priced above $150), particularly Road-150 Red and Mountain-200, consistently drove high profits.
- Seasonal Peaks: Profit concentration occurred mid-year (May–June) and year-end (October–December), varying by year.
- Weekday Advantage: Weekdays contributed more than 70% of profit across all four years, with Thursday ranking in the top 3 every year.
- Customer Drivers: The 50+ age group generated nearly half of total customer profit, and gender impact was nearly balanced.
- Geographic Focus: Australia and the United States accounted for over 60% of total profit.

### Recommendations
- Optimise Product Strategy: Prioritise high-margin items and streamline low-performing SKUs (Stock Keeping Unit).
- Align Campaign Timing: Schedule marketing around seasonal and weekday profit peaks.
- Enhance Customer Segmentation: Target older customers with tailored promotions and loyalty benefits.
- Expand Regional Efforts: Invest further in high-performing markets like Australia and the U.S.
- Reward Top Customers: Establish retention programmes for high-profit individual buyers.

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
