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
* Identify rows with no Boroughs and remove them
* Converts all string columns to uppercase.
* Remove duplicate Collition_IDs to make sure that we are not analysing the same accident more than once
* Creates new columns (TOTAL_KILLED, TOTAL_INJURED, TOTAL_KILLED/INJURED) that will sum up all of the similar columns for simplified analysis.
* Melts multiple “contributing factor” columns into a single column for cause-based analysis.
* Analize what causes we have in our DF and removing errors and blanks



### Analysis and results
* Identification of the most dangerous accident factors in each borough of New York City.
* Presentation of the number of fatalities and injuries caused by speeding in each borough.
* Identification of the three most common accident factors, broken down by borough
* Identification of the three most common accident factors for the entire city overall.
* Determination of the types of vehicles most frequently involved in accidents.
* Statistics on the number of accidents in each borough.
* Most common accident locations