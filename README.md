# Analysis on Popular Restaurants in New York City

This project performs an analysis on popular restaurants in New York City using data scraped from Google Maps and processed using the OpenAI API. 

## Steps

1. **Data Scraping**: The data for the analysis is scraped using Selenium. The information obtained includes the name of the restaurant, category, and related metadata.
2. **Data Cleaning**: The scraped data is cleaned by removing duplicates.
3. **Data Retrieval**: Additional data is retrieved using the Google Places API. This includes getting the Place ID and other details of the restaurant.
4. **Data Processing**: The data is processed to obtain a structured format. This includes extracting information such as the restaurant's opening hours, types of service (dine-in, takeout, etc.), ratings, types, and reviews.
5. **Data Analysis with OpenAI API**: The reviews of the restaurants are analyzed using the OpenAI API. A summary of the reviews is created, extracting information on the cuisine nationality, restaurant type, specialty dishes, strengths of the restaurant, areas for improvement, and an overall summary of the restaurant.
6. **Data Embedding**: The text data is converted into embeddings using OpenAI's text embeddings API. 
7. **Clustering Analysis**: The embeddings are used to perform a clustering analysis. The areas of improvement are clustered using KMeans.The initially assigned clusters were adjusted by GPT model. The clustering results are then visualized using t-SNE.
8. **Closest Restaurant Search**: A function is defined to find the closest restaurant based on different embeddings (Overall Summary, Specialty Dishes, Strengths, and Areas for Improvement).

## Requirements

This project requires the following Python libraries:
- Selenium
- Pandas
- Numpy
- OpenAI API
- sklearn
- requests
- matplotlib
- plotly
- tqdm
- ast
- re
- retrying

## Usage

To use this notebook, you need to provide your Google Maps and OpenAI API keys. Then, run all the cells in the notebook. The notebook will scrape data, process it, and perform analysis on it. The results of the analysis will be displayed in the notebook.

**Note:** Due to the use of the OpenAI API, running this notebook may incur charges.

**Note 2:** The web scraping code is designed to work with Google Maps as of the time of creation. If Google Maps updates their website, the web scraping code may need to be updated. 


## Analysis

Data
<img width="989" alt="image" src="https://github.com/dlworudgg/Popular_Restaurants/assets/37742961/449985fe-0199-47b3-b25c-512016022f70">

2-D t-SNE Visualization
<img width="745" alt="image" src="https://github.com/dlworudgg/Popular_Restaurants/assets/37742961/a98e212b-f629-4335-a8be-c73f6ec34fa0">

3-D t-SNE Visualization
![Area for Improvement 3D t-SNE](https://github.com/dlworudgg/Popular_Restaurants/assets/37742961/9c962292-f266-4ca7-be21-467241c67c49)

Overall Summary of Area for Improvment for top restaurants in New York City
<img width="396" alt="image" src="https://github.com/dlworudgg/Popular_Restaurants/assets/37742961/3965bba3-f3e5-4cf9-a198-08384ee55a45">


## Future Improvements

This notebook could be improved in several ways:
- The data could be updated regularly to reflect changes in the restaurants and their reviews.
- More features could be extracted from the data for more detailed analysis.
- The results of the analysis could be displayed in a more interactive way, such as with interactive plots or a web application.
- The code could be refactored into functions or classes for easier testing and maintenance.
- Error handling could be improved to make the code more robust.
