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
> I have used this project as a foundation to expand my skills and knowledge in data analytics. All credit for the original concept and methodology goes to[Stephen David William](https://www.linkedin.com/in/stephen-david-williams-860428123/).
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
| `POTENTIAL REACH` | The estimated number of people who could see a YouTube video or campaign from this influencer                                                       |

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
I implemented a Python script based on the script developed by Stephen David William, available on [GitHub]([https://github.com/sdw-online](https://github.com/sdw-online/top_uk_youtubers_2024). To see the script I used, just click [here](https://github.com/alejandralopezgalan/alejandralopezgalan.github.io/blob/master/assets/scripts/project2_script_youtube_python.py). 

After running the script, the dataset included four additional columns: `channel_name`,	`total_subscribers`,	`total_views` and `total_videos` as seen in the following image. However, the script did not extract data from two YouTubers, possibly due to unrecognised channel IDs.

{% include figure.liquid path="assets/img/project2_data_updated.png" class="img-fluid rounded z-depth-1" %} 


