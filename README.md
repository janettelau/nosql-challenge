# nosql-challenge
Used MongoDB and Python to evaluate ratings data of various restaurants by the UK Food Standards Agency to help journalists and food critics decide where to focus future articles.

## Tools and Libraries
- Terminal
- MongoDB
- Visual Studio Code
- Python
- Pandas
- PyMongo
- pprint

## Setup and Usage
1. Clone this repository to your local machine:
```
git clone https://github.com/janettelau/nosql-challenge.git
```
2. Import the data from your Terminal using the following command. Instructions for running MongoDB on macOS are provided at the end of the README.
```
mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json
```
3. Navigate to the cloned directory in Visual Studio Code.
4. Open the Jupyter Notebook `NoSQL_setup_starter.ipynb`.
5. Run each cell sequentially to create the database and collection, update the database with the information of the new restaurant, and ensure correct data types.
6. Open the Jupyter Notebook `NoSQL_analysis_starter.ipynb`.
7. Run each cell sequentially to perform exploratory data analysis on hygiene scores and overall ratings.

## Project Breakdown
**Part 1: Database and Jupyter Notebook Setup**
* Imported the data file `establishments.json` from the Terminal.
* Created an instance of the Mongo Client.
* Ensured the database and collection were loaded properly.

**Part 2: Update the Database**
* Added a new restaurant, **Penang Flavours**, to the database.
* Changed the data types of `latitude` and `longitude` from strings to doubles and `RatingValue` from strings to integers.

**Part 3: Exploratory Analysis**
Analyzed the data to answer the following questions:
1. Which establishments have a hygiene score equal to 20?
2. Which establishments in London have a RatingValue greater than or equal to 4?
3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

## Running and Stopping MongoDB on macOS
To Start MongoDB:
* Open a terminal window and run:
```
brew services start mongodb-community@6.0
```
* Then start the MongoDB shell:
```
mongosh
```
* Open a new terminal window and run the `mongoimport` command from earlier.
To Stop the Database and Server:
* Exit MongoDB by pressing `Ctrl + D` or typing `.exit`.
* To stop the MongoDB server, run:
```
brew services stop mongodb-community@6.0
```
