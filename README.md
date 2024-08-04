# Movie Reviews and Details (Data Sourcing with NYT API)

## Requirements
- Python 3.x
- Libraries:
    - requests
    - time
    - python-dotenv
    - os
    - pandas
    - JSON

## NYI Requirement
> Make sure you request your API Key on the NTY site. 

## Project Overview

**1. Access the New York Times API**
This section fetches movie reviews from the New York Times API. It searches for reviews with "love" in the headline, published between January 1, 2013, and May 31, 2023.
The results include fields like headlines, web URLs, snippets, and keywords. The data is collected across multiple pages, normalized, and stored in a DataFrame.

**2. Access The Movie Database API**

Here, the code retrieves detailed movie information from The Movie Database API using the movie titles obtained from the NYT reviews.
For each movie, it gathers details such as budget, genres, spoken languages, production countries, and other relevant data. The results are stored in a DataFrame.

**3. Merge and Clean the Data for Export**

In this section, the data from the NYT reviews and TMDB details are merged based on movie titles.
The combined DataFrame is then cleaned by removing unnecessary characters from certain columns, dropping duplicates, and removing the "byline. person" column.
Finally, the cleaned data is exported to a CSV file.

