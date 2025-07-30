---
layout: page
title: Superstore Sales Analysis
description: An Excel-based project analysing sales data
img: assets/img/project3-ecommerce-web-page.png
importance: 1
category: work
related_publications: false
pretty_table: true
---

{% include figure.liquid loading="eager" max-width="480px" max-height="600px" path="assets/img/project3-online-shopping.png" class="img-fluid rounded z-depth-1" %}
Image from [storyset](https://storyset.com/search?q=online%20shopping)

> **Note**
>
> This project was inspired from Karina Samsonova's data portfolio work featured on her [YouTube channel](https://www.youtube.com/watch?v=U0I3HEnTAWk&ab_channel=KarinaDataScientist). Her comprehensive tutorial on building an interactive Excel dashboard provided guidance throughout my learning journey. 
>
> Original Project:
> 
> Title: Data Analysis Project in Excel - Build Interactive Dashboard. Author: Karina Samsonova Platform: [YouTube](https://www.youtube.com/watch?v=U0I3HEnTAWk&ab_channel=KarinaDataScientist)
>
> This project enhanced my analytical capabilities and expanded my proficiency in data visualisation. Full recognition for the original concept and methodological approach belongs to Karina Samsonova. Her work can be explored further via her [YouTube Channel](https://www.youtube.com/@karinadatascientist) and [LinkedIn](https://www.linkedin.com/in/karina-samsonova/) profile.
<br/>


---
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
  - [Excel Formulae](#excel-formulae)
  - [Data Visualisation](#data-visualisation)
- [Insights](#insights)
- [Action Plan](#action-plan)
  - [1. Customer Acquisition Strategy](#1.Customer-Acquisition-Strategy)
  - [2. Boosting Sales in Q4](#2.-Boosting-Sales-in-Q4)
  - [3. Product and Shipping Optimisation](#3.-Product-and-Shipping-Optimisation)
  - [4. Maximising Regional Performance](#4.-Maximising-Regional-Performance)
  - [5. Customer Retention Initiatives](#5.-Customer-Retention-Initiatives)  
- [Excel Report](#excel-report)	


## Executive Summary
### Primary Goal
The objective is to analyse the Superstore dataset to uncover actionable insights that support strategic business decisions and enhance overall performance. By examining key metrics, such as sales trends, customer demographics, product categories, and regional activity, this analysis aims to identify meaningful patterns, reveal growth opportunities, and address operational inefficiencies.

### Solution
To enable data-driven decision-making, an interactive dashboard will be developed to uncover insights from the Superstore dataset. Tailored for business stakeholders such as sales managers and marketing analysts, this dashboard will visualise:
- Sales trends by time and product category
- Customer demographics and behaviour
- Regional performance breakdowns
The dashboard will empower users to detect patterns quickly, monitor growth drivers, and remedy inefficiencies, ultimately supporting improved strategic outcomes.

### Key Findings and Recommendations
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
            <td>Between 2011–2014, total sales reached $12,642,905 USD across 25,035 unique orders, with an average order value of $505.01 USD.</td>
            <td>Examine if order values or volumes spike during specific periods to align promotions or inventory planning with demand cycles.</td>
            <td>{% include figure.liquid loading="eager" path="assets/img/project3_finding1.png" class="img-fluid rounded z-depth-1" %}</td>
        </tr>
        <tr>
            <td>While overall annual growth was substantial (+90% over three years), no new customers were acquired—potentially due to dataset constraints or insufficient outreach.</td>
            <td>Investigate the dataset’s scope and ensure customer ID tracking is accurate. Missing identifiers may falsely suggest zero acquisition.</td>
            <td>{% include figure.liquid loading="eager" path="assets/img/project3_finding2.png" class="img-fluid rounded z-depth-1" %}</td>
        </tr>
        <tr>
            <td>A recurring Q4 downturn was identified each year, followed by a rebound in early Q1.</td>
            <td>Address Q4 slumps with early festive promotions, bundled top-selling products, and seasonal marketing efforts. </td>
            <td>{% include figure.liquid loading="eager" path="assets/img/project3_finding3.png" class="img-fluid rounded z-depth-1" %}</td>
        </tr>
        <tr>
            <td>Top-performing regions included Asia-Pacific (APAC), United States (US), and Europe (EU). Within these, the US, Australia, and France led in order volume.</td>
            <td>Introduce targeted marketing campaigns and referral incentives in high-performing regions (US, Australia, France) to attract new customers.<br> 
              Strengthen outreach in core markets (APAC, US, EU) via tailored promotions and explore expansion into nearby emerging markets such as Latin America or Eastern Europe.</td>
           <td>{% include figure.liquid loading="eager" path="assets/img/project3_finding4.png" class="img-fluid rounded z-depth-1" %}</td>
        </tr>
        <tr>
            <td>Customers favoured standard class shipping due to its affordability, and consistently selected practical products such as chairs, phones, and storage items.</td>
            <td>Ensure availability for high-demand categories and amplify the benefits of standard class shipping through loyalty rewards.</td>
            <td>{% include figure.liquid loading="eager" path="assets/img/project3_finding5.png" class="img-fluid rounded z-depth-1" %}</td>
        </tr>
        <tr> 
            <td>The majority of purchases were made by individual consumers, rather than businesses or organisations.</td>
            <td>Implement personalised loyalty tiers based on purchasing behaviour, offer customised product recommendations, and improve post-purchase support to encourage repeat business. </td>
            <td>{% include figure.liquid loading="eager" path="assets/img/project3_finding6.png" class="img-fluid rounded z-depth-1" %}</td>
        </tr>
    </tbody>
</table>

## Introduction
This analysis tackles core business challenges through the strategic interpretation of sales data. By leveraging customer segmentation, evaluating product performance, and exploring geographic trends, it identifies key growth levers and operational constraints. The aim is to develop bespoke strategies that enhance customer satisfaction, streamline operations, and drive profitability—laying the foundation for sustainable expansion through informed, data-led decision-making.

### Business Problem
The superstore is experiencing stagnation in customer acquisition and recurring sales declines in the fourth quarter of each year. Despite steady annual growth, no new customers were added between 2011 and 2014, posing a risk to long-term sustainability. Furthermore, demand for high-performing products (e.g., chairs, phones, and storage items) is not being fulfilled efficiently, whilst regional sales strategies lack precision. These issues constrain profitability and hinder expansion. This analysis seeks to uncover performance trends, customer segments, and regional opportunities to craft focused strategies that enhance acquisition, stabilise seasonal sales, and streamline operations.

### Goals
- **Summarise Multi-Year Sales Performance:** Present a high-level overview of superstore sales trends from 2011 to 2014—total revenue, order volumes, average order value, and year-on-year growth—to contextualise historical performance.
- **Highlight Revenue Drivers by Category and Region:** Identify which product categories (e.g. chairs, phones, storage) and regions (APAC, US, EU) contributed most to sales, helping stakeholders focus marketing and inventory efforts.
- **Support Strategic Decision-Making:** Surface actionable visualisations on customer acquisition gaps, shipping preferences, and top markets to inform targeted campaigns, inventory optimisation and regional expansion.
- **Create a Visually Intuitive Dashboard Experience:** Design a clean, coherent Excel dashboard layout with clear labels, logical grouping and straightforward navigation, ensuring accessibility for users of all data-literacy levels.
- **Empower Customer Segmentation Analysis:** Integrate demographic and purchase-type filters to distinguish personal vs. organisational buyers, revealing high-value segments for tailored acquisition and retention strategies.
- **Optimise Shipping Strategy Insights:** Chart shipping-class usage patterns and cost implications to recommend incentives that drive greater adoption of standard-class shipping and reduce fulfilment costs


## Methodology
### Data source
[Kaggle](https://www.kaggle.com/datasets/laibaanwer/superstore-sales-dataset) served as the source for the dataset used in this project. Click [here](https://github.com/alejandralopezgalan/alejandralopezgalan.github.io/blob/master/assets/data/project3_superstore_orders.csv) to access the CSV file directly.

### Data Overview
This dataset provides comprehensive information about the sales of various products offered by the store. It includes related details such as geographical data, product categories and subcategories, sales figures, profit margins, and consumer insights.

| Column name | Description | 
| :--- | :--- |
| `order_id` | A unique identifier assigned to each order | 
| `order_date` | The date on which a customer placed their order | 
| `ship_date` | The shipping date corresponding to the order | 
| `ship_mode` | The shipping method chosen for the order | 
| `customer_name` | The customer's full name. | 
| `segment` | The segment type associated with the order. | 
| `state` | The state where the order was placed. | 
| `country` | The country in which the order was placed. | 
| `market` | The market related to the order. Markets include Africa (Africa), Asia and Pacific (APAC), Canada (Canada), Europe, the Middle East, and Africa (EMEA), Europe (EU), Latin America (LATAM), and the United States of America (US). | 
| `region` | The region within the market where the order was originated. | 
| `product_id` | A unique identifier assigned to each product. | 
| `category` | The product's main category. | 
| `sub_category` | The product's subcategory. | 
| `product_name` | The name of the product. | 
| `sales` | The total sales revenue generated for an order, measured in US dollars. | 
| `quantity` | The number of products included in each order. | 
| `discount` | The discount applied to the order. | 
| `profit` | The profit generated from the sale of an order. | 
| `shipping_cost` | The shipping cost incurred for the order. | 
| `order_priority` | The priority level assigned to each order. | 
| `year` | The year in which the order was placed. | 

<br/>

### Tools
- Excel: Used for exploring, cleaning, analysing, and visualising the data through a dashboard.


### Data Cleaning and Transformation
After importing the dataset into Excel and converting the file into an Excel Worksheet, the data was transformed into an Excel Table to facilitate easier management and analysis. The dataset already included a year column; however, it was beneficial to use an Excel formula to extract the year from the `order_date` column. First, the `order_date` column was formatted as a Date. Then, an Excel formula was applied to extract the year, which was subsequently formatted as a number without decimals and named `order_year`.

In most businesses, each customer is assigned a unique customer ID; however, this variable was missing in the dataset. By leveraging the `customer_name` variable, it was possible to identify unique customers using a conditional Excel formula that counts each time a new customer is added to the database. This new variable was named `customer_unique`. A similar approach was taken to count the unique number of orders. Using the `order_id` column, a conditional formula was applied to count unique order IDs. This newly created variable was named `order_unique`.

### Data Analysis
The initial step involved estimating four KPIs using Pivot Tables: Total Sales (USD), Number of Unique Orders, and Number of Unique Customers. Additionally, a calculated field was created to estimate the Average Sales per Order (USD), with the result displayed to two decimal places.

Pivot Tables were then used to calculate Total Sales by Quarter and Total Sales by Year, employing the `order_year` variable to analyse sales trends over time.

To evaluate regional performance, a Pivot Table was created to examine Total Sales by Market. Another Pivot Table identified the Top 10 Countries Leading in Total Sales (USD).

For customer insights, a Pivot Table estimated the Total Sales (USD) for three segments: Consumer, Corporate, and Home Office. Additionally, customer preferences for shipping modes were analysed by calculating the percentage of total orders for each mode.
Finally, product insights were derived using Pivot Tables to review Total Sales (USD) by Product Category and Subcategory, as well as the Top 10 Best-Selling Products (USD).


### Excel formulae

|Formula|Description| 
|:---|:---|
|`=YEAR([@[order_date]])`|Extract the Year from the order date|
|`=IF(COUNTIF(F$2:F2,F2)=1,1,0)` | Count each unique customer. Assigns a value of 1 if the customer is unique and 0 if the customer is repeated|
|`=IF(COUNTIF(A$2:A2,A2)=1,1,0)` | Counts each unique `order_id`. Assigns a value of 1 if the `order_id` is unique and 0 if repeated|
|`Avg Sales per Order = sales/ order_unique`| A calculated field used to estimate the average sales per order|

<br/>

### Data Visualisation
Using the insights derived from the pivot tables, the next step involved creating a series of visuals to include in the dashboard. First, two slicers for `order_year` and `market` were added to enable filtering across the visuals.
The values from four KPIs—**Total Sales (USD), Number of Unique Orders, Number of Unique Customers,** and **Average Sales per Order (USD)**—were displayed at the top of the dashboard using four cards.
To illustrate the **Sales Trend**, two charts were created: a line chart showing the **Quarterly Breakdown of Total Sales (USD)** and a bar chart depicting the **Annual Sales Performance (USD)**.

{% include figure.liquid loading="eager" path="assets/img/project3_dashboard1.png" class="img-fluid rounded z-depth-1" %}

To analyse **Regional Performances**, a vertical bar chart was used to present the **Market-Wise Breakdown of Total Sales (USD)**, while a horizontal bar chart highlighted the **Top 10 Countries Leading in Total Sales (USD)**.
{% include figure.liquid loading="eager" path="assets/img/project3_dashboard2.png" class="img-fluid rounded z-depth-1" %}


For **Customer Insights**, two charts were added: one showing the **Total Sales Distribution Across Customer Segments** and the other highlighting **Customer Preferences for Shipping Modes**, expressed as a percentage of total orders.
{% include figure.liquid loading="eager" path="assets/img/project3_dashboard3.png" class="img-fluid rounded z-depth-1" %}


Finally, for **Product Insights**, a bar chart displayed the **Total Sales (USD) by Product Category and Subcategory**, accompanied by a table listing the **Top 10 Best-Selling Products (USD)**.
{% include figure.liquid loading="eager" path="assets/img/project3_dashboard4.png" class="img-fluid rounded z-depth-1" %}


Watch a brief video showcasing the full dashboard here:
{% include video.liquid path="assets/video/project3_video_dashboard.mp4" class="img-fluid rounded z-depth-1" controls=true %}


## Insights
- Between 2011 and 2014, total sales reached $12,642,905 USD, generated from 25,035 unique orders placed by 795 customers, with an average order value of $505.01 USD 
- According to the data, the Superstore has not acquired any new unique customers since 2011, but sales and the number of unique orders have steadily increased year after year.  
- Over the past three years, sales consistently declined in the final quarter of each year; however, they tended to increase again in the following year.  
- From 2011 to 2014, annual sales rose by $2,040,530, reflecting an impressive growth of approximately 90%.  
- Asia-Pacific (APAC), the United States (US), and Europe (EU) consistently ranked as the top three markets, solidifying their status as the cornerstone of the Superstore's global success.  
- During this period, the United States, Australia, and France led as the countries with the highest number of orders placed.  
- Most customers are individuals purchasing goods or services for personal use rather than organisational needs.  
- The majority of customers preferred lower shipping costs, opting for the standard class shipping mode.  
- The top-selling products included chairs, phones, and storage items, showcasing customer preferences for functional and versatile items across various categories.  

{% include figure.liquid loading="eager" path="assets/img/project3_insights1.png" class="img-fluid rounded z-depth-1" %}
{% include figure.liquid loading="eager" path="assets/img/project3_insights2.png" class="img-fluid rounded z-depth-1" %}
{% include figure.liquid loading="eager" path="assets/img/project3_insights3.png" class="img-fluid rounded z-depth-1" %}

## Action plan
A recommended action plan tailored to the trends and observations from the analysis:

### 1. Customer Acquisition Strategy
   - **Issue Identified**: No new unique customers since 2011.  
   - **Implementation roadmap**:  
     - Launch targeted marketing campaigns (e.g., social media, email) focused on acquiring new customers.  
     - Offer referral incentives to existing customers for bringing in new buyers.  
     - Partner with influencers or businesses in your top-performing regions (US, Australia, France) to reach untapped audiences.

### 2. Boosting Sales in Q4
   - **Issue Identified**: Declining sales during the last quarter of each year.  
   - **Implementation roadmap**:  
     - Implement Q4-exclusive promotions or discounts (e.g., holiday or end-of-year sales).  
     - Begin pre-holiday marketing campaigns earlier to create anticipation.  
     - Focus on top-performing product categories (chairs, phones, storage items) and bundle them for holiday gifting.  

### 3. Product and Shipping Optimisation
   - **Issue Identified**: Customers prefer affordable shipping and practical, versatile products.  
   - **Implementation roadmap**:  
     - Strengthen inventory of top-selling products (e.g., chairs, phones, storage items).  
     - Offer discounts or loyalty points for selecting standard shipping to further encourage its use.  
     - Explore partnerships with shipping companies to reduce overall delivery costs.

### 4. Maximising Regional Performance
   - **Insight**: APAC, US, and EU are top markets, and US, Australia, and France lead in orders.  
   - **Implementation roadmap**:  
     - Tailor region-specific promotions or exclusive product lines to reinforce loyalty in these markets.  
     - Identify emerging markets near these regions for possible expansion (e.g., Canada, New Zealand, or nearby EU countries).  
     - Conduct customer surveys to better understand regional preferences and adapt offerings accordingly.

### 5. Customer Retention Initiatives
   - **Insight**: Most clients are individual consumers.  
   - **Implementation roadmap**:  
     - Develop a customer loyalty programme with personalised rewards.  
     - Offer personalised recommendations based on past purchases to encourage repeat orders.  
     - Enhance post-purchase support to ensure customer satisfaction and strengthen brand loyalty.

## Excel Report
To review the analysis in detail, you can download the Excel Report [here.](https://github.com/alejandralopezgalan/alejandralopezgalan.github.io/blob/master/assets/data/project3_superstore_orders_report.xlsx)
