# nosql-challenge
Hello in this repository you will see that there is a Starter_Code file with two jupyter notebooks one is a NoSQL_setup_starter.ipynb  and the other an analysis_starter. There is a resource file inside the Starter_Code file that has the data used to make the dataframes in the jupyter notebooks.
Finally you have the README file which you are reading right now. Hello!
# Background
The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. I've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.
## Part 1: Database and Jupyter Notebook Set Up
Go to NoSQL_setup_starter.ipynb for this section of the project.
I imported the data provided in the establishments.json file from my gitbash Terminal. I named the database uk_food and the collection establishments. 

-Within the notebook, the following libraries had been imported : PyMongo and Pretty Print (pprint).

-Created an instance of the Mongo Client.

-Confirmation that I created the database and loaded the data properly:

-Listed the databases I have in MongoDB. Confirm that uk_food is listed.

-List the collection(s) in the database to ensure that establishments is there.

-Find and display one document in the establishments collection using find_one and display with pprint.

-Assign the establishments collection to a variable to prepare the collection for use.

## Part 2: Update the Database

See NoSQL_setup_starter.ipynb for this section of the project.

The magazine editors have some requested modifications for the database before I can perform any queries or analysis for them. I have to make the following changes to the establishments collection:

-An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. The magazine has asked me to include it in my analysis

-Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.

-Update the new restaurant with the BusinessTypeID that was found.

-The magazine is not interested in any establishments in Dover, so I had to check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.

-Some of the number values are stored as strings, when they should be stored as numbers.

-Use update_many to convert latitude and longitude to decimal numbers.

-Use update_many to convert RatingValue to integer numbers.

## Part 3: Exploratory Analysis

Eat Safe, Love has specific questions they want me to answer, which will help them find the locations they wish to visit and avoid.

Look to NoSQL_analysis_starter.ipynb for this section of the project.

Some notes to be aware of while you are exploring the dataset:

RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating.

The scores for Hygiene, Structural, and ConfidenceInManagement work in reverse. This means, the higher the value, the worse the establishment is in these areas.

Using the following questions to explore the database(listed below), and find the answers, so I can later provide them to the magazine editors.

Unless otherwise stated, for each question:

Use count_documents to display the number of documents contained in the result.

Display the first document in the results using pprint.

Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.

1. Which establishments have a hygiene score equal to 20?

2. Which establishments in London have a RatingValue greater than or equal to 4?

3. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.
