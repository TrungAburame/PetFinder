# Description
During the time learn how to use the SSIS, I came to realize that "why don't we create a proper pipeline to show the employer my greenest Data Engineering data pipeline ever?"

# Context
There is a PetFinder Company that collecting homeless dogs and cats from around the ASEAN, temporary feed them until they are moving to their new home.
The raw data file was extracted from the system as CSV. Sample are shown below.

![image](https://user-images.githubusercontent.com/72678942/212987326-78790afd-f39b-4650-91f3-e9445190eef2.png)

Our mission is to create a pipeline that collect this CSV file to all the way to a proper dashboard report for analytics!

# Data Pipeline tools Diagrams
The tools we are using today include:
  Source: CSV
  ETL: Visual Data Studio + MS server (or SSIS)
  Database: MS server
  Visualization: Power BI

![datapipeline](https://user-images.githubusercontent.com/72678942/212994570-ebfbcfd9-e727-41ee-ad58-8991c73efa9a.jpg)

# Relational Diagram
Here we use Star Schema databases which are best used for historical data. This makes them work most optimally for data warehouses, data marts, BI use and OLAP.

![assignment1 draw io](https://user-images.githubusercontent.com/72678942/213174249-481e141b-8a6d-464a-9265-e1deaf9e9960.png)

# ETL
Initial Load: For the first time uploading data after created all the necessary tables.

![image](https://user-images.githubusercontent.com/72678942/213177122-85270735-a31a-4485-ac39-5a54add6751f.png)

Incremental Load: Eventhough the Data flow task look at lot simpler, incremental load actually took me more time where I have to check whether the data in DIM table already existed or not. If yes, base on the table concept, I need to decide whether I should keep the historical data or not.

![image](https://user-images.githubusercontent.com/72678942/213177403-3b29a58c-b8ed-452c-a721-ec97fd98f372.png)

# Visualization
Finally, I import data into Power BI from MS SQL. We could see that both dogs and cats are not vaccinated yet. Mainly because they were homeless.
However the gap between vaccinated compared to not vaccinated cats are way bigger than dogs. It is proved that more dog got a home before being homeless.
Over than half of pets are black, brown is the second most popular with 29% of dogs and 14% of cat are brown.

![image](https://user-images.githubusercontent.com/72678942/213178681-69d64fbc-5a1b-4d2a-8fb1-b734dada42f1.png)

