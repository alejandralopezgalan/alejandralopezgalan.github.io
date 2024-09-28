---
layout: page
title: HR Metrics Monitoring and Attrition Analysis
description: A guided project from DataCamp [Data Analyst in Power BI track](https://app.datacamp.com/learn/career-tracks/data-analyst-in-power-bi) about HR analytics
img: assets/img/12.jpg
importance: 1
category: work
related_publications: false
---

## Table Of Contents

- [Executive Summary](#executive-summary)
  - [Key Findings](#key-findings)
  - [Recommendations](#recommendations)
- [Introduction](#introduction)
  - [Business Problem](#business-problem)
  - [Goals](#goals)
  - [Data Source](#data-source)
  - [Tools and Techniques](#tools-and-techniques)
- [Methodology](#methodology)
  - [Data Exploration and Cleaning](#data-exploration-and-cleaning)
    - [Data Understanding](#data-understanding)
    - [Data Cleaning](#data-cleaning)
    - [Data Transformation](#data-transformation)
  - [Data Analysis](#data-analysis)
    - [Key Metrics and KPIs](#key-metrics-and-kpis)
    - [Data Visualization](#data-visualization)
- [Results and Implications](#results-and-implications)


---
## Executive Summary
The primary goal of this project was to establish a comprehensive system for monitoring key HR metrics and employee performance. Secondary to this, the project aimed to identify the primary factors influencing employee attrition within the organisation.

By analysing various employee and company data points, I was able to uncover significant insights into the drivers of turnover.

### Key Findings

- The majority of employees are between 20 and 29 years old, and currently the company, Atlas Labs, employs 2.7% more women than men, with a total of 1233 active employees.
- Employees who identify as non-binary make up 8.5% of total employees.
- Employes who identify as white have the highest average salary, whereas mixed or multiple ethnic groups have one pf the lowest average salaries. 
- The attrition rate is 16.1% and the department and job role with the highest attrition rate is Sales and Sales Representative, respectively.
- Departmental disparities: Sale consistently experienced higher turnover rates than other departments.
- Managerial rating level and self-performance level do not always align. 

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
