---
layout: page
title: Top 100 YouTubers from Mexico
description: A project to analyse the top 100 YouTubers from Mexico
img: assets/img/project2_top-youtubers.png
importance: 1
category: work
related_publications: false
pretty_table: true
---


{% include figure.liquid loading="eager" max-width="480px" max-height="600px" path="assets/img/project2_portada_influencer.png" class="img-fluid rounded z-depth-1" %}
Image from [storyset](https://storyset.com/search?q=video%20influencer)

> **Note**
>
> This project was inspired and guided by the work of Stephen David William on [GitHub](https://github.com/sdw-online), whose data portfolio project provided invaluable insights and direction. I deeply appreciate the effort and dedication Stephen put into creating such a comprehensive resource.
>
> Original Project Title: Excel to Power BI Portfolio Project. Full End-to-End Data Project. Top_uk_youtubers_2024. Author: Stephen David William. Platform: [YouTube](https://www.youtube.com/watch?v=mm_sN-Elplg&t=510s&ab_channel=Stephen%7CData)
>
> I have used this project as a foundation to expand my skills and knowledge in data analytics. All credit for the original concept and methodology goes to [Stephen David William](https://www.linkedin.com/in/stephen-david-williams-860428123/).
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
  - [Tools](#tools)
  - [Data Cleaning](#data-cleaning)
  - [Extracting data from YouTube](extracting-data-from-youtube)
  - [Data Transformation in SQL](#data-transformation-in-sql)
  - [Analysis in Power BI](#analysis-in-power-bi)
    - [DAX measures](#dax-measures)
    - [Data Visualisation](#data-visualisation)
  - [Data Analysis for the Marketing Campaign](#data-analysis-for-the-marketing-campaign)
    - [YouTubers with the most subscribers](#youtubers-with-the-most-subscribers)
    - [YouTubers with the most total views](#youtubers-with-the-most-total-views)
    - [YouTubers with the most videos uploaded](#youtubers-with-the-most-videos-uploaded)
- [Insights](#insights)
    - [Collaboration Recommendations](#collaboration-recommendations)
    - [Potential Return on Investment](#potential-return-on-investment)
- [Action Plan](#action-plan)	 

---
## Executive Summary
### Primary Goal
Identify the top YouTubers from Mexico in 2024 to determine which influencers are best suited for running successful marketing campaigns throughout the rest of the year.

### Solution
Develop a dashboard to provide insights into the top Mexican YouTubers in 2024, showcasing their subscriber count, total views, total videos, and engagement metrics. This tool will support the marketing team in making informed decisions about which YouTubers to collaborate with for their campaigns.

### Key Findings
- Fede Vigevani, YOLO AVENTURAS, and Badabun have the highest number of subscribers, attracting a large audience with their engaging content.
- Badabun leads in the volume of videos uploaded, followed by Tlnovelas and Tu COSMOPOLIS, demonstrating their commitment to consistently providing fresh content.
- Channels such as Masha y el Oso, YOLO AVENTURAS, and Badabun are recognised for their popularity and video views, showcasing their widespread influence in the region.

### Recommendations
- Collaborate with Fede Vigevani to maximise visibility, as this channel has the most YouTube subscribers in Mexico and the highest average views per video.
- Consider potential partnerships with Masha y el Oso and YOLO AVENTURAS, as they attract high engagement on their channels consistently.
- Avoid influencer marketing campaigns with the channels that have the most videos uploaded (Badabun, Tu COSMOPOLIS, and Tlnovelas) due to lower potential return on investment.
- Reach out to the Fede Vigevani team to negotiate contracts within allocated budgets, kick off campaigns, track performance, review progress, gather insights, and optimise based on feedback from converted customers and each channel's audiences.
- Explore potential partnerships with other influencers such as Masha y el Oso and YOLO AVENTURAS in the future.

---

## Introduction

### Business Problem
The marketing team needs to identify and collaborate with the most influential Mexican YouTubers to maximise the effectiveness of their marketing campaigns. Currently, they lack a comprehensive and easily accessible tool that provides insights into key metrics such as subscriber count, total views, total videos, and engagement metrics. This gap hinders their ability to make informed decisions about which YouTubers to partner with for optimal campaign performance.

### Goals
1. Develop an Interactive Dashboard: Create a user-friendly dashboard using Power BI to visualise data on the top Mexican YouTubers in 2024.
2. Data Collection and Integration: Gather comprehensive data on subscriber counts, total views, total videos, and engagement metrics for the top YouTubers in Mexico.
3. Insight Generation: Analyse the collected data to identify trends and patterns among the top YouTubers.
4. Support Informed Decision-Making: Equip the marketing team with actionable insights to identify the best YouTubers for collaboration.
5. Customisable Features: Allow for customisable views and filters within the dashboard to cater to the specific needs and preferences of the marketing team.

---
## Methodology

### Data source

The dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/bhavyadhingra00020/top-100-social-media-influencers-2024-countrywise?resource=download). To view the CSV file, click [here](https://github.com/alejandralopezgalan/alejandralopezgalan.github.io/blob/master/assets/data/project2_youtube_data_mexico.csv).

This dataset provides structured information about the top 100 YouTubers from Mexico in 2024. Each entry represents a YouTuber and includes the following attributes:

| Column name          | Description                                                                                                                                      | 
| :------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------- |
| `#`                  | The ranking of the YouTuber in the top 100 list                                                                                                  |
| `NAME`               | The name or pseudonym of the YouTuber                                                                                                            |
| `FOLLOWERS`          | The total number of subscribers the influencer has on YouTube                                                                                    |
| `ER`                 | Engagement Rate: The level of interaction that the influencer's content receives from users on social media platforms, expressed as a percentage |
| `COUNTRY`            | The geographical location or country where the YouTuber is based or primarily operates                                                           |
| `TOPIC OF INFLUENCE` | The niche or category in which the YouTuber specialises or creates content, such as fashion, beauty, technology, fitness, etc.                   |
| `POTENTIAL REACH`    | The estimated number of people who could see a YouTube video or campaign from this influencer                                                    |

<br/>

### Tools
- Excel: To explore the data.
- PostgreSQL: To clean, test, and analyse the data.
- Power BI: To visualise the data via interactive dashboards.
- GitHub: To host the project documentation and version control.

### Data Cleaning
Displayed below is a screenshot of a portion of the data presented in Excel.

{% include figure.liquid path="assets/img/project2_kaggle_data_original.png" class="img-fluid rounded z-depth-1" %} 

The objective is to refine our dataset, ensuring it is well-structured and primed for analysis.

Criteria for the cleaned data:
- Retain only the pertinent columns.
- Ensure all data types are suitable for their respective columns.
- Verify that no column contains null values, guaranteeing the completeness of all records.

After the initial data exploration, I realised that some columns, such as `ER`, `COUNTRY`, and `TOPIC OF INFLUENCE`, are either irrelevant for our analysis or have missing values. Considering our primary goal and the desired solution, the dataset should contain information related to subscriber count, total views, total videos, and engagement metrics. Therefore, I needed to extract this information from YouTube to complement our dataset. I used a Python script to extract this information from YouTube.

### Extracting data from YouTube
I implemented a Python script based on the script developed by Stephen David William, available on  [GitHub](https://github.com/sdw-online/top_uk_youtubers_2024). To see the script I used, just click [here](https://github.com/alejandralopezgalan/alejandralopezgalan.github.io/blob/master/assets/scripts/project2_script_youtube_python.py). 

After running the script, the dataset included four additional columns: `channel_name`,	`total_subscribers`,	`total_views` and `total_videos` as seen in the following image. However, the script did not extract data from two YouTubers, possibly due to unrecognised channel IDs.

{% include figure.liquid path="assets/img/project2_data_updated.png" class="img-fluid rounded z-depth-1" %} 

The script output found no data on these two channels, even though they actually exist on YouTube. Therefore, I decided to manually enter this data using the information from the 'About' section of these YouTube channels. I added this information at the end of the table so I could use Excel or SQL to sort the channels by their respective ranks based on `total_subscribers`,	`total_views` and `total_videos` later on. 

{% include figure.liquid path="assets/img/project2_script_output.png" class="img-fluid rounded z-depth-1" %} 

For the following steps, I used PostgreSQL. I changed the column names to lowercase with dashes instead of spaces and renamed the column `rank` instead of `#`n Excel before loading the data into SQL. The updated dataset can be found [here](https://github.com/alejandralopezgalan/alejandralopezgalan.github.io/blob/master/assets/data/project2_updated_youtube_data_mex.csv) and the following image shows a view of this dataset.

{% include figure.liquid path="assets/img/project2_database_for_sql.png" class="img-fluid rounded z-depth-1" %} 


### Data Transformation in SQL
I developed a SQL script for data cleaning. For a detailed review of the script, click [here](assets/scripts/project2_sql-script-youtubers-mx.sql). The steps involved in the scripts were:
1. Create the database.
2. Create the table to store YouTube data.
3. Import the data into the newly created table and verify proper loading.
4. Create a view to simplify the data by selecting specific columns: `channel_name`, `total_subscribers`, `total_views` and `total_videos`.
5. Perform data quality checks:
 - a. Verify the number of rows: Top 100 YouTube channels.
 - b. Verify the number of columns: `channel_name`, `total_subscribers`, `total_views` and `total_videos`
 - c. Check the data type of each variable.
 - d. Check the number of unique channels in the database or count the number of duplicate channels.
6. Create a new table to export the data to a CSV file. To see the output file, click this [link](assets/data/project2_mx_youtubers_data2024.csv).

{% include figure.liquid path="assets/img/project2_database_view_sql.png" class="img-fluid rounded z-depth-1" max-width="550px" max-height="500px" %} 


**SQL code** 
```sql  
-- Create the database
CREATE DATABASE youtube_mx_db;

-- Create the table to store YouTube data
CREATE TABLE IF NOT EXISTS youtube_mx
(
    rank smallint,
    name character varying(100),
    followers character varying(50),
    er character varying(50),
    country character varying(50),
    topic_of_influence character varying(50),
    potential_reach character varying(50),
    channel_name character varying(100),
    total_subscribers integer,
    total_views bigint,
    total_videos integer
);

/* After importing the data into the newly created table, 
verify that the data was properly loaded */
SELECT * 
FROM youtube_mx
LIMIT 10;

-- Create a view to simplify the data by selecting specific columns 
/* To practice SQL, you can create a view with the following columns: 

CREATE VIEW view_mex_youtubers AS 
	SELECT SUBSTRING(name, 1, strpos(name, '@') -1)::VARCHAR(100) AS 
		channel_name, total_subscribers, total_views, total_videos FROM youtube_mx; 
*/ 

/* However, since the channel_name is already correctly formatted from the Python script, 
and I manually entered stats for two channels at the end of the table, 
we will create the view with these columns:
*/
CREATE view view_mex_youtubers AS
	SELECT
		channel_name,
 		total_subscribers, 
 		total_views,
 		total_videos
 	FROM
 		youtube_mx;

-- Data quality check: 
-- Verify the number of rows (Top 100 YouTube channels)
SELECT
	COUNT(*) AS num_rows
FROM
	view_mex_youtubers;

-- Verify the number of columns 
-- (channel_name, total_subscribers, total_views, total_videos)
SELECT 
	COUNT(*) AS column_count
FROM
	information_schema.columns
WHERE 
	TABLE_NAME ='view_mex_youtubers';

-- Check the data type of each variable
SELECT 
	column_name,
	data_type
FROM
	information_schema.columns
WHERE 
	TABLE_NAME ='view_mex_youtubers';

-- Check the number of unique channels in the database
SELECT
	COUNT(DISTINCT(channel_name)) AS unique_channels
FROM
	view_mex_youtubers;

-- Alternatively, count the number of duplicate channels
SELECT 
	channel_name,
	COUNT(*) AS duplicates
FROM 
	view_mex_youtubers
GROUP BY channel_name
HAVING COUNT(*) > 1;

-- Create a new table to export the data to a CSV file
CREATE TABLE mexicans_youtubers AS
	SELECT
		channel_name,
 		total_subscribers, 
 		total_views,
 		total_videos
 	FROM
 		youtube_mx;

-- Review the table
SELECT *
FROM mexicans_youtubers
LIMIT 10;
   ```  

### Analysis in Power BI
I loaded the CSV file [mx_youtubers_data2024](assets/data/project2_mx_youtubers_data2024.csv) into a Power BI report, and the following image showed that the variables were correctly loaded.

{% include figure.liquid path="assets/img/project2_data_loaded-powerbi.png" class="img-fluid rounded z-depth-1" max-width="450px" max-height="400px" %} 

#### DAX measures
I constructed a table with all the essential measures for the analysis, employing DAX formulas to develop these metrics.

**1. `AvgViewsPerVideo(M)`** <br />
Computes the average number of views per video, expressed in millions, for a YouTube channel.
```sql  
AvgViewsPerVideo(M) =
  VAR sumtotalviews = SUM(mx_youtubers_data2024[total_views])
  VAR sumofvideos = SUM(mx_youtubers_data2024[total_videos])
  VAR avgviewspervideo = DIVIDE(sumtotalviews, sumofvideos, BLANK())
  VAR avgviewspervideomillions = DIVIDE(avgviewspervideo, 1000000, BLANK())

  RETURN avgviewspervideomillions
```
<br />

**2. `SubscriberEngagementRate`** <br />
Calculates the average number of subscribers per video for a YouTube channel.
```sql  
SubscriberEngagementRate =
  VAR sumtotalsubscribers = SUM(mx_youtubers_data2024[total_subscribers])
  VAR sumtotalvideos = SUM(mx_youtubers_data2024[total_videos])
  VAR subscribersengrate = DIVIDE(sumtotalsubscribers, sumtotalvideos, BLANK())

  RETURN subscribersengrate
```
<br />

**3. `TotalSubscribers(M)`** <br />
Converts the total number of subscribers into millions, making it easier to interpret large subscriber counts.
```sql  
TotalSubscribers(M) =
  VAR million = 1000000
  VAR sumofsubscribers = SUM(mx_youtubers_data2024[total_subscribers])
  VAR totalsubscribers = DIVIDE(sumofsubscribers, million)

  RETURN totalsubscribers
```
<br />

**4. `TotalVideos`** <br />
Sums up the total number of videos for a YouTube channel.
```sql  
TotalVideos =
  VAR totalvideos = SUM(mx_youtubers_data2024[total_videos])

  RETURN totalvideos
```
<br />

**5. `TotalViews(B)`** <br />
Converts the total number of views into billions, providing a clearer representation of large view counts.
```sql  
TotalViews(B) =
  VAR billion = 1000000000
  VAR sumoftotalviews = SUM(mx_youtubers_data2024[total_views])
  VAR totalviews = DIVIDE(sumoftotalviews, billion, BLANK())

  RETURN totalviews
```
<br />

**6. `ViewsPerSubscriber`** <br />
Determines the total number of views each subscriber has generated, offering insights into how engaged the subscriber base is with the channel's content.
```sql  
ViewsPerSubscriber =
  VAR sumtotalsubscribers = SUM(mx_youtubers_data2024[total_subscribers])
  VAR sumofviews = SUM(mx_youtubers_data2024[total_views])
  VAR viewspersubscriber = DIVIDE(sumofviews, sumtotalsubscribers, BLANK())

  RETURN viewspersubscriber
```

#### Data Visualisation

The dashboard consist of: 
1. Table of the Top 100 YouTubers: This table presents the most popular YouTube influencers, showcasing data on their total number of subscribers (in millions), the aggregate number of videos, and the overall views (in billions).
2. Treemap of the Top 10 YouTubers: This treemap illustrates the top 10 YouTubers by their total views (in billions). Each segment delineates a YouTuber, accompanied by data on their total number of videos and subscribers (in millions).
3. Channel Engagement Ratios: Three cards present essential engagement metrics.
   - Average Views per Video: The mean number of views each video generates.
   - Subscriber Engagement Rate: A metric quantifying the extent of subscribers' engagement with the content.
   - Views per Subscriber: The average number of views generated per subscriber.
4. Bar Chart of the Top 10 YouTubers: This bar chart ranks the top 10 YouTubers based on their total number of subscribers (in millions), providing a visual representation of their popularity.

{% include figure.liquid path="assets/img/project2_dashboard.png" class="img-fluid rounded z-depth-1" %} 

The interactive features of this dashboard:
1. Table Interactivity: The table facilitates sorting and filtering of the top 100 YouTubers by subscribers, videos, or views. Selecting a YouTuber's name could present detailed insights into their channel's performance.
2. Treemap Interactivity: Hovering over each segment of the treemap unveils additional information regarding the YouTuber's total videos and subscribers. Selecting a segment could navigate to a more detailed analysis of that YouTuber's channel analytics.
3. Engagement Cards Interactivity: The cards dynamically update as different YouTubers are selected from the table or treemap, enabling the comparison of engagement metrics across channels.
4. Bar Chart Interactivity: The bar chart permits highlighting and comparison of the top 10 YouTubers by total subscribers. Hovering over each bar displays a tooltip with more comprehensive subscriber information.

{% include figure.liquid path="assets/img/project2_video_dashboard.gif" class="img-fluid rounded z-depth-1" %} 


### Data Analysis for the Marketing Campaign
Based on the information and the data analysis I have done so far, it is possible to continue with the marketing analysis for the campaign. First, I focused on the following questions:

1. Who are the top 10 YouTubers with the most subscribers?

| Rank | Channel                                            | Subscribers (M) |
| :--- |:-------------------------------------------------- | --------------: |
| 1    | Fede Vigevani                                      | 62.30           |
| 2    | YOLO AVENTURAS                                     | 58.50           |
| 3    | Badabun                                            | 47.60           |
| 4    | Kimberly Loaiza                                    | 46.30           |
| 5    | Juan De Dios Pantoja                               | 44.00           |
| 6    | Masha y el Oso                                     | 39.60           |
| 7    | GENIAL                                             | 32.00           |
| 8    | YOLO                                               | 31.90           |
| 9    | Susy Mouriz                                        | 27.30           |
| 10   | BabyBus - Canciones Infantiles & Videos para Niños | 26.80           |

<br />

