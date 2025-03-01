# nosql-challenge
Using MongoDB and Python to evaluate ratings data of various restaurants by the UK Food Standards Agency to help journalists and food critics decide where to focus future articles.

## Tools and Libraries
- Terminal
- Visual Studio Code
- Python
- Pandas
- PyMongo
- pprint

## Setup and Usage
1. Clone this repository to your local machine.
```
git clone https://github.com/janettelau/nosql-challenge.git
```
2. Import the data from your Terminal using the following command.
```
mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json
```
3. Navigate to the cloned directory in Visual Studio Code.
4. Open the Jupyter Notebook `NoSQL_setup_starter.ipynb`.
5. Run each cell sequentially to create the database and collection, update the database with the information of the new restaurant, and ensure correct data types (Parts 1 and 2).
6. Open the Jupyter Notebook `NoSQL_analysis_starter.ipynb`.
7. Run each cell sequentially to perform exploratory data analysis on hygiene scores and overall ratings (Part 3).

## Project Breakdown
**Part 1: Database and Jupyter Notebook Setup**
* Imported the data file `establishments.json` from the Terminal.
* Created an instance of Mongo Client.
* Ensured the database and collection have been loaded properly.

**Part 2: Update the Database**
* Updated the database with the information of the new restaurant, "Penang Flavours".
* Changed the data types of `latitude` and `longitude` from strings to doubles and `RatingValue` from strings to integers.

**Part 3: Exploratory Analysis**
Analyzed the data to answer the following questions:
1. Which establishments have a hygiene score equal to 20?
2. Which establishments in London have a RatingValue greater than or equal to 4?
3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.
