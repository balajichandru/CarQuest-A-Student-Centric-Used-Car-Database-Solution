# CarQuest-A-Student-Centric-Used-Car-Database-Solution
CarQuest: A Student-Centric Used Car Database Solution

### Project Overview

Reliable, economical, and environmentally friendly transportation options are in high demand in today’s changing automotive market, which has resulted in a sharp increase in the appeal of used vehicles. But for prospective buyers, sorting through the wide selection of available cars can be a difficult undertaking. It might take a lot of time and energy to sort through internet listings, find reliable information, and come to a well-informed selection. Our idea aims to introduce a state-of-the-art platform into the used car industry in order to tackle this difficulty. This platform makes use of a strong database system to expedite the search procedure and give consumers an easy-to-use interface. Our goal is to improve data security, accessibility, and accuracy by switching from traditional spreadsheet-based methods to a dynamic database architecture.

### Data Source- https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data

### Tools and Technologies used:

- PostGRESQL Database- DBMS tool
- Python- Data Processing and Manipulation
- VS Code- IDE 
- NodeJS- Web User Interface

### Project duration- Sept 01, 2023 to Dec 01, 2023

### Highlights-

- Data cleaning and refining
- Normalization of data using 1NF, 2NF, 3NF, BCNF, 4NF
- ER diagram design

[![ER Diagram](https://github.com/arjunsai07/CarQuest-A-Student-Centric-Used-Car-Database-Solution/blob/main/ER%20diagram.png?raw=true "ER Diagram for CarQuest")

- Insertion of records into the database tables
- Creating queries for CRUD operations
- Creating a webUI to access the database and provide an interface for the users
  
### List of tables

- Car_Region: Enlists details about the car's region(State)
- Car_Location: Provides details about the latitude and longitude of the car's location
- Car_Model: Describes details on the car's make and manufacturer
- Car_Entry: Contains entries of various used cars available in New York State
- Car_Identification: Describes the physical attributes of the car, like the look-and-feel
- Car_Specification: Provides details on the car's usage, like the odometer reading

### Usage of indexing to speed up the database access 

*     Car Region Table: In the creation of the Car_Region table, we have the implicit index column RegionID. This is a key column that is unique to each row in the table and thus helps to quickly locate and access the data.

*     Car Location Table:
      Primary Key Index: LocationID serves as the primary key, acting as an implicit index.
      Foreign Key Index: RegionID is used to refer to the Car_Region table, functioning as a foreign key index that speeds up join operations between the Car_Region and Car_Location tables.

*     Car Model Table:
      Primary Key Index: The primary key on ModelID simplifies the search for car models.
*	  Car Entry Table:
      Primary Key Index: The Vehicle Identification Number (VIN) is the unique identifier for each car, ensuring effective retrieval of each car entry listing.
      Foreign Key Index: The foreign keys LocationID and ModelID reference the Car_Location and Car_Model tables, respectively.

### DATABASE Operations Performed

- **SELECT QUERY**:
  -   List All Cars with Their Location
  -   Find Cars with Specific Manufacturer in a Given Region
  -   Average Price of Each Car Model
  -   Top 5 Expensive Car Models in Each Region
  -   Finding Cars with Specific Color and Condition
  -   Cars with Mileage Over 100,000 by Manufacturer
  -   Latest Models Available in Each State
- **INSERT QUERY**:
  -   Data was collated in Python [Python Data Processing](https://github.com/arjunsai07/CarQuest-A-Student-Centric-Used-Car-Database-Solution/blob/main/CarQuest%20SourceCode.ipynb "Python Data Processing")
  -   Initial data had a **huge amount** of data. We condensed the data to only include used-cars data related to NY state alone.
  -   From this **condensed dataset**, we performed normalization to make the data clean and void of redundancy.
  -   Created dataframes corresponding to the 6 tables and inserted them from Python(VSCode) to PostGRESql database in appropriate tables.
- **UPDATE AND DELETE QUERY**:
  -   Performed **cascading update** on the Car_Region table, such that if the RegionID table is updated, Car_Location table also gets updated automatically.
  -   Same was tried with **cascading delete** operation.
- **QUERY EXECUTION ANALYSIS**:
  -   Identified problematic queries which took an extended period of time to finish execution.
  -   Approached the problem as a 2-step solution. Observed the execution time of the query before and after performing indexing.
  -   Used **Explain tool** available in PostGRESql to observe the execution plan of the query.
  -   Created indexes for frequently accessed columns and observed the consequential improvement in execution time.


### CarQuest WebUI

-  CarQuest, our online tool, redefines the used car search experience. With an intuitive and user-friendly interface, CarQuest aims to provide a seamless and efficient way for users to
explore, compare, and discover used cars.
-  The project ensures that users can find the perfect vehicle that meets their preferences and requirements.
-  The website was run in our local machine. The deployment of the same is planned for a future release.


[![WebUI Snapshot 1](https://github.com/arjunsai07/CarQuest-A-Student-Centric-Used-Car-Database-Solution/blob/main/WebUI%20Sc1.png "WebUI Snapshot 1")

[![WebUI Snapshot 2](https://github.com/arjunsai07/CarQuest-A-Student-Centric-Used-Car-Database-Solution/blob/main/WebUI%20Sc2.png "WebUI Snapshot 2")

[![WebUI Snapshot 3](https://github.com/arjunsai07/CarQuest-A-Student-Centric-Used-Car-Database-Solution/blob/main/WebUI%20Sc3.png "WebUI Snapshot 3")

[![WebUI Snapshot 4](https://github.com/arjunsai07/CarQuest-A-Student-Centric-Used-Car-Database-Solution/blob/main/WebUI%20Sc4.png "WebUI Snapshot 4")

### Authors

- **Arjun Srinivasan** - [https://github.com/arjunsai07](https://github.com/arjunsai07")
- **Sai Teja** - bsaiteja43@gmail.com
- Balaji Hariharan

### Acknowledgments

- Kaggle, for providing the dataset
- Microsoft, for the VSCode IDE
- PostGRESQL https://www.postgresql.org/docs/
- Node JS https://nodejs.org/en/about
  


