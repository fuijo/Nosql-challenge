# nosql-challenge

This project involved analyzing food hygiene ratings data from the UK Food Standards Agency to assist the food magazine Eat Safe, Love in identifying focus areas for future articles. The project consisted of three main parts: database setup, data updates, and exploratory analysis.

**Part 1: Database and Jupyter Notebook Setup**
**Objective:** Prepare the database and confirm the data is correctly loaded for analysis.

The establishments.json file was imported into a MongoDB database named uk_food with a collection named establishments.
**MongoDB commands were executed to:**
List available databases and collections, confirming the presence of uk_food and establishments.
Display one sample document using find_one() and pprint.
The establishments collection was assigned to a variable for subsequent queries.
Outcome: Database setup was successfully completed and validated.

**Part 2: Update the Database**
**Objective:** Modify the data to align with the magazine's requirements.

**Adding a New Restaurant:**

A new restaurant, Penang Flavours, was added to the database with the provided details.
The BusinessTypeID for "Restaurant/Cafe/Canteen" was queried and updated in the new restaurant’s document.
Removing Unwanted Records:

Establishments under the "Dover Local Authority" were identified and deleted. The deletion was confirmed by checking document counts before and after the operation.
Data Type Corrections:

Latitude and longitude fields were converted from strings to decimal numbers.
The RatingValue field was converted from strings to integers for numeric consistency.
Outcome: Database modifications were implemented as specified.

**Part 3: Exploratory Analysis**
**Objective:** Answer specific questions using MongoDB queries and Python data analysis tools.

**Hygiene Score of 20:**

Queried establishments with a hygiene score of 20, returning 41 results.
Results were converted to a Pandas DataFrame for further inspection.
High-Rated Establishments in London:

Located establishments in London with a RatingValue ≥ 4 using a regex-based search.
Retrieved 33 establishments and presented the data in a DataFrame.
Top 5 High-Rated Establishments Near "Penang Flavours":

Queried establishments within 0.01 degrees of Penang Flavours' location, with RatingValue = 5.
Results were sorted by hygiene score and limited to the top 5 establishments.
Results were converted to a DataFrame for visualization.
Local Authority Hygiene Scores:

Aggregated data to count establishments with a hygiene score of 0, grouped by Local Authority.
Results were sorted in descending order and presented as a DataFrame, displaying the top 10 authorities.
Outcome: Insights were successfully derived, providing valuable information for the magazine editors.

**Deployment and Submission**
All work was submitted to a GitHub repository with appropriate commit messages.
Code was well-commented to ensure clarity and ease of understanding for future developers.
Key Outcomes for the Magazine
Identification of establishments with the highest and lowest hygiene scores for potential coverage.
A detailed list of top-rated establishments in London for high-profile reviews.
A focused analysis of Local Authority areas with the most hygiene concerns.
This project established a strong foundation for Eat Safe, Love to make data-driven editorial decisions, enhancing its value to readers interested in food hygiene standards.
