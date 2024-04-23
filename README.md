###### distance-education-highered_ MADS Capstone

# Distance Learning in Higher Education: <br> Past Trends and Future Forecasts
Team 25 EduTrends

[Overview](https://github.com/katyk20/distance-education-highered#overview) <br>
[Getting Started](https://github.com/katyk20/distance-education-highered?tab=readme-ov-file#getting-started)<br>
[Project Datasets](https://github.com/katyk20/distance-education-highered?tab=readme-ov-file#project-datasets) <br>
[Data Sources](https://github.com/katyk20/distance-education-highered?tab=readme-ov-file#data-sources) <br>
[Project Notebook Descriptions](https://github.com/katyk20/distance-education-highered?tab=readme-ov-file#notebook-descriptions) <br>


## Overview
Welcome to our data-driven exploration of higher education distance learning. In this project, we're applying data science techniques to analyze tabular data and sentiment from Reddit posts to understand the trends that have shaped higher education distance education from 2018 to 2022. 

For clarity, distance education (DE) is defined as instruction delivered through various technologies (e.g., internet, satellite, audio/video conferencing), enabling interaction between students and instructors, whether synchronously or asynchronously. A course is classified as DE if instructional content is exclusively delivered through DE methods, while a program is labeled DE if students can fulfill all required coursework via DE courses (NCES IPEDS, 2024)

### Why it Matters
Understanding trends in distance education is crucial for higher education institutions to adapt and thrive in a rapidly evolving landscape. By providing data-driven insights, we aim to support informed planning and decision, as well as help institutions prepare for the future.

### What We're Doing:
- Data Analysis: Using higher education student demographics along with DE enrollment and DE program offering to uncover patterns and insights from the past few years.
- Sentiment Analysis: By examining sentiments expressed in Reddit discussions about distance education, we aim to understand public perceptions and concerns.
- Time Forecasting: Leveraging our findings, we'll attempt to forecast future directions in distance learning, offering valuable insights for strategic decision-making.

### Read our:
:page_facing_up: [Final report](https://docs.google.com/document/d/1hAFd8SASDJH0lxrD4ig_5FWExbkLXo5Cbv4rfN_gOLE/edit?usp=drive_link)

:pen: [Medium Blog Post -"Article Title TBD"](https://medium.com/@katy.kibbey/distance-education-title-c188a963fb9b)

:pushpin: [Project poster](https://docs.google.com/presentation/d/13iPOYDqoVSwNZCOwiQMkazkkIz-5QQ2I/edit?usp=drive_link&ouid=110253943311085891145&rtpof=true&sd=true)

:bar_chart: [Public Tableau-hosted Visualizations](https://public.tableau.com/views/DistanceLearning_17124483932140/map_enrollment_unit_tot?:language=en-US&publish=yes&:sid=&:display_count=n&:origin=viz_share_link)

<div class='tableauPlaceholder' id='viz1712529958339' style='position: relative'><noscript><a href='#'>
 <p align="center">
 <img alt='map_enrollment_unit_tot ' 
src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Di&#47;DistanceLearning_17124483932140&#47;map_enrollment_unit_tot&#47;1_rss.png' style='border: none' /></a></p></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='DistanceLearning_17124483932140&#47;map_enrollment_unit_tot' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Di&#47;DistanceLearning_17124483932140&#47;map_enrollment_unit_tot&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>            


## Project Management

### Getting Started

### Installation- Option 1
1. Get a copy of this project by simply running the git clone command to create a local repository 
```git
git clone <https://github.com/katyk20/DistanceLearning_Capstone.git>
``` 
2. Install dependencies
 ```git
pip install -r requirements.txt
```  
### Installation- Option 2
If you prefer running the code in Google Colab and accessing dataset files stored in Google Drive, follow these steps:

1. Go to [Google Colab](https://colab.research.google.com/). Sign in with your Google account if you haven't already.<br>
2. In Google Colab, click on "File" -> "New notebook" to create a new notebook.<br>
3. In the Colab interface, click File/Open/ “GitHub,” enter the GitHub URL, and hit the search icon.<br>
4. In a code cell of your new notebook, mount your Google Drive to access its contents.
 ```git
from google.colab import drive
drive.mount('/content/drive')
```
5. Clone our project repository into your Google Drive.
 ```git
!git clone <https://github.com/katyk20/DistanceLearning_Capstone.git> '/content/drive/My Drive/path/to/your/repository'
```
### Project Datasets
6. Upload our project datasets and models to the data/ folder within your Colab environment for easy access during runtime. All final cleaned and prepared datasets used in this project can be accessed [here](https://drive.google.com/drive/folders/18Fxc3f10pHkkCEgaC65efWkRxm6e7XCM?usp=drive_link)
   

## Data Sources
1. [National Center for Education Statistics (NCES) Integrated PostSecondary Education Data System (IPEDS)](https://nces.ed.gov/ipeds/datacenter/DataFiles.aspx?goToReportId=7&sid=91e3bacc-b5ed-4fd5-b314-96ea78985bdd&rtid=1)

IPEDS  is a system of survey components that collects data from all institutions that provide postsecondary education and are eligible to receive Title IV funding across the United States and other U.S. jurisdictions. IPEDS begain tracking DE in 2021-2013 and currently collects DE data in four survey components:
* ***Institutional Characteristics***: Records institutions offering DE courses and/or programs for undergraduate and graduate students and whether all programs are offered exclusively via DE.  <br>
* ***12-Month Enrollment***:number of students enrolled in DE courses over 12-month period.<br>
* ***Fall Enrollment***: Captures the number of students enrolled in DE courses in the fall term and, of the students enrolled exclusively via DE, by degree level and geographic location.<br>
* ****Completions****: Captures whether all, some, or none of the programs within each CIP-coded academic program and award level can be completed entirely via DE.<br>

The table below shows specific NCES IPEDS data surveys (and dictionaries) used in this project:
Years | Survey | Title| Files
--- | --- | --- | ---
2012-022 |Institutional Characteristics | Directory Information | [Link](https://drive.google.com/drive/folders/1NrNxFucUF7sCDtOA2jhnsagqmNo6VpKa?usp=drive_link)
2012-2022 |Fall Enrollment| Race/ethnicity, gender, attendance status, and level of student: Fall YEAR | [Link](https://drive.google.com/drive/folders/1RC1T14lLjWJ1ZRXSDybccV7XKtc7Xbjc?usp=drive_link)
2012-2022|Fall Enrollment| Age category, gender, attendance status, and level of student: Fall YEAR | [Link](https://drive.google.com/drive/folders/12aRk50aV3HM1vpqOq5xl_TffNeRiVuAf?usp=drive_link)
2012-2022 |Fall Enrollment| 	Distance education status and level of student: Fall YEAR | [Link](https://drive.google.com/drive/folders/1xqpvpyMAU3S_EePQY-7xKcXCuuKvU6Du?usp=drive_link)
2012-2022 |Completions | 	Number of programs offered and number of programs offered via distance education, by award level: July 1, YEAR to June 30, YEAR| [Link](https://drive.google.com/drive/folders/1HEIRoYDmd8-dsfApnnjX7zll8G6jRmMO?usp=drive_link)

Additionally, the [CIP SOC Crosswalk](https://docs.google.com/spreadsheets/d/1AmHnURaSmVWcB8-CUC7G9naCyCCRuTjS/edit?usp=drive_link&ouid=110253943311085891145&rtpof=true&sd=true) was retrieved. The crosswalk matches 6-digit CIP Codes from the 2020 Classification of Instructional Programs (CIP) with 6-digit detailed descriptions from the 2018 Standard Occupational Classification (SOC) used in Bureau of Labor and Statistics Occupational Projections datasets. The purpose of the crosswalk is to match postsecondary programs of study that provide graduates with specific skills and knowledge to occupations requiring those skills or knowledge to be successful (NCES IPEDS, 2024. 


2. [U.S. Bureau of Labor and Statistics (BLS)](https://www.bls.gov/emp/data/occupational-data.htm)
Data accessed from BLS to create modeling dataset included:
-  The Occupational Projections Data database (Table 1.7) displays data on employment, employment change, occupational openings, education, training, and wages for each detailed National Employment Matrix occupation. 
-  The Current Employment Statistics (CES) program produces detailed industry estimates of nonfarm employment, hours, and earnings of workers on payrolls. Employment by industry was accessed and merged with Occupational Projections data on industry codes.
-  State Unemployment rates 2018-2022.

BLS datasets can be accessed [here](https://drive.google.com/drive/folders/1TioSuaNFfEJH-TbDDYhHzKX5E3TBgosr?usp=drive_link)

3. [The-Eye Subreddit Archives](https://the-eye.eu/redarcs/) - Through The-Eye subreddit archives we collected data from the following subreddits:
- **r/education** - This subreddit archive has over 100 million datapoints from 2005-2022. This is a complete archive of every post and comment ever made within this subreddit. We combined the comments with to each post and refined the dates to 2018-2022. Additionally, we performed sentiment analysis on each comment and post, as well as performing an emotional tone score.
- **r/highereducation** - This subreddit archive has over 50 million datapoints from 2012-2022. This is a complete archive of every post and comment ever made within this subreddit. We combined the comments with to each post and refined the dates to 2018-2022. Additionally, we performed sentiment analysis on each comment and post, as well as performing an emotional tone score.

The subreddit notebooks and datasets can be found [here](https://drive.google.com/file/d/1QoLfg6w4E-nSlG1SyqUnqVBjHA1YIigr/view?usp=share_link)


## Notebook Descriptions
#### Tabuluar Dataset Preparation [![Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://github.com/katyk20/distance-education-highered/blob/main/Notebooks/NCES_IPEDS_Dataset.ipynb)
This notebook merges yearly IPEDS survey data into one file with necessary pre-processing. 
Four distinct data files (.csv) are created:
* age_gen_by_inst_18_22.csv: 2018-2022 age, gender, attendance status, and level of student merged with institutional variables of interest. (Note: This is all institution students- not DE specifically.)
* race_gen_by_inst_18_22.csv: 2018-2022 race/ethnicity gender, attendance status, and level of student merged with institutional variables. (Note: This is all institution students- not DE specifically.)
* dist_enrollment18_22.csv: 2018-2022 fall DE enrollment merged with institutional variables of interest.
* depprogramsoffered18_22.csv: 2018-2022 completions survey data merged with institutional variables of interest. 

#### Exploratory Data Analysis [![Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://github.com/katyk20/distance-education-highered/blob/main/Notebooks/EDA.ipynb)
We conducted a variety of EDA on our NCES IPEDS datasets filtering deeper into DE subcategories (e.g. private vs public institutions, in-state vs. out-of-state students).

#### r/Education Dataset Preparation, Sentiment Analysis, and Emotional Tone Analysis [![Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://drive.google.com/file/d/1QoLfg6w4E-nSlG1SyqUnqVBjHA1YIigr/view?usp=sharing)
We imported, clean, prepped, and performed sentiment and emotional tone analysis on the r/education subreddit.

 #### r/HigherEducation Dataset Preparation, Sentiment Analysis, and Emotional Tone Analysis [![Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://drive.google.com/file/d/19D6Oz_vbFQi90Zp1pdXS9iH2xXavOdK9/view?usp=sharing)
We imported, clean, prepped, and performed sentiment and emotional tone analysis on the r/highereducation subreddit.

#### Emotion Tone Distribution by Year [![Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://drive.google.com/file/d/19D6Oz_vbFQi90Zp1pdXS9iH2xXavOdK9/view?usp=sharing)
Based on the combined subreddit data we plotted the emotional tone distribution by the years 2018-2022.

#### Time Forecasting Models - [![Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://github.com/katyk20/distance-education-highered/blob/main/Notebooks/TimeForecasting_ExpSmooth(Univariate).ipynb))  [![Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)](https://github.com/katyk20/distance-education-highered/blob/main/Notebooks/TimeSeriesForecasting(Univariate)2.ipynb)) We attempt to conduct 5-year forecasting using statistical and ML modeling, including the use of  PyCaret machinge learning library. 

## License
This project is licensed under MIT License- see the LICENSE file for details

## Authors
Katy Kibbey<br>
Jeff Park<br>
Jeffrey Roscyzk

## Acknowledgements
Thank you to Dr.Elle O'Brien, Team25 Advisor Winston Featherly-Bean, and our fellow MADs Capstone peers for your resources and guidance.
