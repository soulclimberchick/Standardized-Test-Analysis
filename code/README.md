# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

### Overview

Our first module in DSI covers:
- Basic statistics and probability
- Many Python programming concepts
- Programmatically interacting with files and directories
- Visualizations
- EDA
- Working with Jupyter notebooks for development and reporting

For this first project, I am going to take a look at aggregate SAT and ACT scores and graduation rates at four-year colleges in the United States.

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.

### Problem Statement

Many folks are questioning the necessity of standardized SAT and ACT tests as a means for preparation and measurement of college readiness in the United States. 
Here, I aim to discover whether there is any correlation between SAT and ACT scores in relation to attainment for a bachelor's degree (graduation rate) at a four-year college in the United States.


If we find that there is no positive correlation - meaning better test scores = better success rate, it may be time to consider what the purpose of these tests are. 

If we find that there is a positive correlation, colleges and universitites may reconsider the current trend of makign these trends optional as a means to acceptance into these institutions.

---

### Datasets

#### Provided Data

**Chosen Given Datasets:**

`sat_act_by_college.csv:` Ranges of Accepted ACT & SAT Student Scores by Colleges\
`sat_2017.csv:` 2017 SAT Scores by State\
`sat_2018.csv:` 2018 SAT Scores by State\
`sat_2019.csv:` 2019 SAT Scores by State\
`act_2017.csv:` 2017 ACT Scores by State\
`act_2018.csv:` 2018 ACT Scores by State\
`act_2019.csv:` 2019 ACT Scores by State

#### Additional Data

**Data Sets from US Department of Education College Scorecard**  

URL: https://collegescorecard.ed.gov/data/documentation/  

`MERGED2016_17_PP.csv:` 2016-2017 Aggregated data including SAT, ACT scores and college completion rates by college.
`MERGED2017_18_PP.csv:` 2017-2018 Aggregated data including SAT, ACT scores and college completion rates by college.
`MERGED2018_19_PP.csv:` 2018-2019 Aggregated data including SAT, ACT scores and college completion rates by college. 

### Deliverables

- A Jupyter notebook that describes your data with visualizations & statistical analysis.
- A README markdown file the provides an introduction to and overview of this project.
- A presentation slideshow rendered as a .pdf file.

---

### Data Dictionary

Much of this data dictionary gleaned and adapted from included data.yaml file for US Department of Education College Report Card

Data URL: https://collegescorecard.ed.gov/data/documentation/

File located in dir data/CollegeScorecard_Raw_Data/'data.yaml'

It can be provided upon request
Can also be found in the data download from the provided url for the DECSC data set

The following data definitions are the column names used for visualizations and presentation and include the edited and formatted names that differ from the original data sources. All else are excluded as they were not used for the analysis and presentation. 

Key:

    source: column name
    type: data type
    description: description


    source: state
    description: State postcode

    source: sat_avg
    type: float
    description: Average SAT equivalent score of students admitted

    source: satvrmid
    type: float
    description: Midpoint of SAT scores at the institution (critical reading)

    source: satmtmid
    type: float
    description: Midpoint of SAT scores at the institution (math)

    source: satwrmid
    type: float
    description: Midpoint of SAT scores at the institution (writing)

    source: actcmmid
    type: float
    description: Midpoint of the ACT cumulative score

    source: actenmid
    type: float
    description: Midpoint of the ACT English score

    source: actmtmid
    type: float
    description: Midpoint of the ACT math score

    source: ACTMIDWR
    type: float
    description: Midpoint of the ACT writing score

    source: act_avg
    type: float
    description: Average SAT equivalent score of students admitted

    source: deg_type
    type: integer
    description: |-
      Highest degree awarded
       0 Non-degree-granting
       1 Certificate degree
       2 Associate degree
       3 Bachelor's degree
       4 Graduate degree

    source: grad_rate
    type: float
    description: Completion rate for first-time, full-time bachelor's-degree-seeking
      students at four-year institutions (200% of expected time to completion)

    source: p_cred_lev
    type: integer
    map: program
    descripton: "Level of credential
      Credentials are categorized into the following levels:
      1: Undergraduate Certificate or Diploma
      2: Associate's Degree
      3: Bachelor's Degree
      4: Post-baccalaureate Certificate
      5: Master's Degree
      6: Doctoral Degree
      7: First Professional Degree
      8: Graduate/Professional Certificate"

## Functions:

source: calc_mean  
variables: takes data set (num)  
description: a function to check for zero values, then calculate the mean of a set of values

source: calc_std  
variables: takes data set (num)  
description: a function to check for zero values, then calculate the standard deviation of a set of values

source: clean_percent  
variables: takes a string (data)  
description: a function to check for '%' value and removes them using data.replace

source: clean_x  
variables: takes a string (data)  
description: a function to check for 'x' value and removes them using data.replace

source: clean_dash  
variables: takes a string (data)  
description: a function to check for '-' value and removes them using data.replace

source: title_lower  
variables: takes a string (column_title)  
description: a function to convert capital letters to lowercase


