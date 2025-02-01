# Analiza-Danych-Pandas-Pawel-Kossowski

## Table of Contents
* [General Info](#general-info)
* [Setup](#setup)
* [Code Exlanation](#Code-Explanation)

## General Info

The project involves analyzing data from the nypd-motor-vehicle-collisions.csv dataset to examine motor vehicle accidents in New York City. The analysis includes data ingestion, cleaning, transformation, and visualization of results. Key aspects include identifying the most dangerous accident factors by borough, determining fatalities and injuries caused by speeding, analyzing the three most common accident causes (both citywide and by borough), identifying the types of vehicles most frequently involved in accidents, providing accident statistics for each borough and identifying the most frequent accident locations. Findings will be presented with visualizations, along with conclusions.


## Setup

To get started with this project, follow these steps:

1. Clone the repository:

    ```bash
    git clone https://github.com/Pawelk1234/Analiza-Danych-Pandas-Pawel-Kossowski
    ```

2. Install the required dependencies using the `requirements.txt` file:

    ```bash
    pip install -r requirements.txt
    ```
3. Download the required data file:

   You will need to download the dataset from Kaggle. Use the following link to access the dataset:

   https://www.kaggle.com/datasets/new-york-city/nypd-motor-vehicle-collisions

   Save the downloaded file in the project directory.

Now you're ready to run the project!

## Code Explanation
Below is an outline of the logical flow in the provided code:

### Data Cleaning
* Converts all string columns to uppercase.
* Drops duplicate collision entries using COLLISION_ID.
* Creates new columns (TOTAL_KILLED, TOTAL_INJURED, TOTAL_KILLED/INJURED) for simplified analysis.
* Melts multiple “contributing factor” columns into a single column for cause-based analysis.
### Exploratory Analysis
* Identifies the top 3 collision causes per borough in terms of both frequency and severity (injuries/kills).
Examines patterns specifically related to unsafe speed accidents.
Visualizes the most common accident causes across different boroughs.
Vehicle Type Analysis
Melts multiple “vehicle type” columns into a single column for simplified analysis of vehicle types involved.
Geospatial Visualization
Uses osmnx to retrieve the geometry for New York City.
Uses geopandas to create geospatial points from the dataset’s latitude/longitude columns.
Plots collision points on a map of NYC (only a subset of points for demonstration if needed).
Results
Use this section to include any final charts, numerical findings, or interpretations you derived from the analysis. Possible examples include:

Top Contributing Factors (e.g., driver inattention, failure to yield, etc.)
Borough with Highest Number of Accidents
Most Severe Types of Collisions (in terms of injuries/fatalities)
Notable Trends (e.g., speeding issues, certain vehicle types more involved)
Insert your findings, graphs, and interpretations here.