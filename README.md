# UK Food Establishment Data Management

### Introduction
This project is dedicated to the comprehensive management of UK food establishment data. The key tasks involve setting up a MongoDB database named `uk_food` and a collection named `establishments`. The workflow encompasses importing data, updating the database with new information, and conducting exploratory analysis. The analysis aims to extract insights into hygiene scores, restaurant types, and ratings.

### Database and Jupyter Notebook Setup
#### Import Data
To initiate the database, import data from the provided `establishments.json` file into MongoDB. This can be accomplished using the following command in the Terminal:

```bash
mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json
```

#### Setup without Code
1. **MongoDB Connection**: Ensure that MongoDB is installed and running on your system. Confirm the connection to the MongoDB instance.

2. **Database Creation**: Create a new database named `uk_food`.

3. **Collection Creation**: Establish a collection named `establishments` within the `uk_food` database.

4. **Data Import**: Utilize the provided `establishments.json` file to import data into the `establishments` collection.

5. **Verify Setup**: Confirm the successful creation of the database and collection. Explore a sample document in the `establishments` collection to ensure proper setup.

### Update the Database
1. **Add a New Restaurant - "Penang Flavours"**: Add a new restaurant entry for "Penang Flavours" to the database. Include relevant details such as business name, address, and local authority information.

2. **Find and Return BusinessTypeID and BusinessType for "Restaurant/Cafe/Canteen"**: Identify the BusinessTypeID for the category "Restaurant/Cafe/Canteen" and return relevant information.

3. **Update the New Restaurant with the Correct BusinessTypeID**: After identifying the BusinessTypeID, update the entry for "Penang Flavours" with the accurate BusinessTypeID.

4. **Check and Remove Establishments within the Dover Local Authority**: Investigate and determine the number of documents associated with the Dover Local Authority. Remove all establishments within this authority and validate the deletion.

5. **Convert Number Values to Decimal and Integer Types**: Modify data types as needed, such as converting latitude and longitude to decimal numbers. Ensure that rating values are in the appropriate integer format.

### Exploratory Analysis
#### 1. Establishments with Hygiene Score of 20
   - Identify and examine establishments with a hygiene score of 20. Display the number of documents, the first document, and the first 10 rows in a Pandas DataFrame.

#### 2. Establishments in London with RatingValue >= 4
   - Find and explore establishments in London with a RatingValue greater than or equal to 4. Display the number of documents, the first document, and the first 10 rows in a Pandas DataFrame.

#### 3. Top 5 Establishments with RatingValue = 5, Sorted by Lowest Hygiene Score, Nearest to "Penang Flavours"
   - Execute a query to find the top 5 establishments with a RatingValue of 5, sorted by the lowest hygiene score. Display the results.

#### 4. Establishments in Each Local Authority Area with Hygiene Score of 0
   - Develop a pipeline to:
      1. Match establishments with a hygiene score of 0.
      2. Group the matches by Local Authority.
      3. Sort the matches from highest to lowest. Display the number of documents and the first 10 results in a Pandas DataFrame.

#### 5. Convert Results to CSV
   - Export the resulting DataFrame to a CSV file for future reference.

### Instructions
To execute the project and access the data:

1. Confirm the presence of the required libraries and dependencies.
2. Run the Python script to perform data management and analysis.
3. Review the resulting 'output.csv' file for the gathered data and analysis results.