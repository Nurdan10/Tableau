# Data Visualization with Tableau
## Covid-19 Tracking Dashboard
### Overview
COVID-19 is the infectious disease caused by the coronavirus, SARS-CoV-2, which is a respiratory pathogen. World Health Organization first learned of this new virus from cases in Wuhan, People’s Republic of China on 31 December 2019.

<center class="img-fluid" alt="label">
<img src="https://drive.google.com/uc?export=view&amp;id=11yLhtbPmrhXvVXNM375yaz-6g76T_BnP" alt="covid-19" width="500" height="300">
</center>

### Objective
This project requires you to explore given data set, design interactive dashboard, and then convey your results in a website through Google Sites. 

### Instructions
There are 3 milestones (1 optional) in the project.
#### Acquiring & Loading the Dataset to MS SQL Server with Python - First Milestone
*  Download the dataset from https://data.world via [this link](https://query.data.world/s/oo7wqc57rmotflrwykyjexbuz7tuue?dws=00000). (You can also read the dataset directly from the link but this increases the reading time dramatically.)
* Assign the dataset to a pandas `df`. It will be better to set the `low_memory` parameter of `read_csv` to `False`.
* Update the column names with lowercase.
* As you learned in SQL Course;
    - Connect to MS SQL Server via both `pyodbc` and `sqlalchemy`, (You should connect to the `master` database because you will create a database via python),
    - Create a database named `Covid19` via `pyodbc` conneciton
    - Create a schema named `covid` in `Covid19` database (You can create via both `pyodbc` and `sqlalchemy`),
    - Load the df (so the dataset) to `Covid19` database in MS SQL Server. Set the both table and schema name `covid` (You can load via both `pyodbc` and `sqlalchemy` but `sqlalchemy` is the easiest way).
#### Creating Dashboard - Second Milestone
* The full dataset is a large one and may need extra computing time when creating views in Tableau depending on your computer's hardware spesifications. Therefore, we only select a certain part of the data.
* In *Tableau Desktop Professional Edition*;
    * Go to Connect > To a Server > Microsoft SQL Server and connect to the your local MS SQL Server.
    * Drag the `New Custom SQL` to Canvas and add the SQL query which retrieves the dataset of `report_date` between '
    `2022-01-01` and `2022-04-30`.
* In *Tableau Desktop Public Edition*;
    * Go to Connect > To a File > Text file and connect to the csv file.
    * Add a `Data Source Filter` which filters the dataset of `report_date` between '
    `2022-01-01` and `2022-04-30`.
* Create an interactive dashboard.
#### Creating a Google Site - Third Milestone (Optional)
* Create a Google site. Choose a meaningful site name that reflects your site's purpose. 
Please refer to the following link on how to create a google site:
https://support.google.com/sites/answer/98081?hl=en
* You can choose a background image from [unsplash.com](https://unsplash.com/) or any other source.
* Embed the your interactive dashboard to your web site and publish.
