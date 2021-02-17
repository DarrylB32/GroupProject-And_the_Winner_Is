# GroupProject-And_the_Winner_Is
This repository has been copied from it's original location [HERE](https://github.com/bkaczor00/ETL-Project), so that future updates and changes made by me will not effect the other authors. To see ALL commits to the project please refer to the original.

The purpose of this project is to undergo the extract, transform and load (ETL) process to find the create a list of Academy Award winners and their movies. We used a CSV of all [Academy Award Data](data_csv.csv) ranging from 1927 - 2017 and [The Movie Database API](https://developers.themoviedb.org/3/getting-started/introduction). The [oscar.ipynb](oscar.ipynb) file details the Extraction and Transformation of the data, which was then loaded into SQL using pgAdmin.

### Data
* [Academy Award Winners spanning from 1927 - 2017](https://datahub.io/rufuspollock/oscars-nominees-and-winners#resource-data)
* [The Movie Database API](https://developers.themoviedb.org/3/getting-started/introduction)
---
### Tech Stack
* Python
* pgAdmin
* Jupyter Notebook
* Excel

### User Instructions
* Clone the repository: git clone https://github.com/DarrylB32/GroupProject-And_the_Winner_Is.git 
* Open and execute [oscar.ipynb](oscar.ipynb) file.
* Establish SQL database to query from
* Import the new [tables](Output) into your database
* Open the [pgAdminQuery](Output/pgAdminQuery.sql) schema in your SQL database and execute each statement
* Run your own custom queries

### Authors
* Darryl Baynes
* [Beth Kaczor](https://www.linkedin.com/in/bethkaczor/)
* [Kathryn Rigsby](https://www.linkedin.com/in/kathrynrigsby/)
* [Jen Kwon]()


### Additional Notes
**Tables**

 - actor_actress 
	 - Includes year of the award win, the award category,
   winner = True, and actor/actress name. It’s used to store the main
   data that other tables can reference to if wanting to view everything
   at once.

 - actor_id
	 - Includes entity (Actor/Actress first and last name) and ID number (unique key)
Because some actors/actresses have won multiple years we needed to drop the duplicates in order to create a primary key.

 - actor_id_title
	 - Includes the actor/actress IDs (as a foreign key) and all of the movies they’ve been in.