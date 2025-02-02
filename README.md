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
    * Staten Island
        * Driver Inattention/Distraction - 5,453
        * Failure to Yield Right-of-Way - 2,956
        * Following Too Closely - 1,240
    * Queens
        * Driver Inattention/Distraction - 41,106
        * Failure to Yield Right-of-Way - 23,857
        * Traffic Control Disregarded - 8,230
    * Manhattan
        * Driver Inattention/Distraction - 24,964
        * Failure to Yield Right-of-Way - 9,611
        * Following Too Closely - 3,588
    * Brooklyn
        * Driver Inattention/Distraction - 39,075
        * Failure to Yield Right-of-Way - 23,653
        * Traffic Control Disregarded - 9,180
    * Bronx
        * Driver Inattention/Distraction - 18,597
        * Failure to Yield Right-of-Way -8,609
        * Traffic Control Disregarded -4,028
* Presentation of the number of fatalities and injuries caused by speeding in each borough.
    * BRONX - 2,240
    * BROOKLYN - 3,808
    * MANHATTAN - 1,040
    * QUEENS - 3,043
    * STATEN ISLAND - 570.0 
* Identification of the three most common accident factors, broken down by borough
    * Bronx
        * Driver Inattention/Distraction – 29,952
        * Failure to Yield Right-of-Way – 7,923
        * Backing Unsafely – 7,658
    * Brooklyn
        * Driver Inattention/Distraction – 63,866
        * Failure to Yield Right-of-Way – 25,114
        * Backing Unsafely – 15,665
    * Manhattan
        * Driver Inattention/Distraction – 71,360
        * Failure to Yield Right-of-Way – 14,803
        * Turning Improperly – 13,161
    * Queens
        * Driver Inattention/Distraction – 73,704
        * Failure to Yield Right-of-Way – 27,953
        * Backing Unsafely – 16,784
    * Staten Island
        * Driver Inattention/Distraction – 10,541
        * Failure to Yield Right-of-Way – 3,227
        * Backing Unsafely – 2,447
* Identification of the three most common accident factors for the entire city overall.
    * Driver Inattention/Distraction – 249,423
    * Failure to Yield Right-of-Way – 79,020
    * Backing Unsafely – 53,810
* Determination of the types of vehicles most frequently involved in accidents.
    * Passenger Vehicle – 927,454
    * Sport Utility / Station Wagon – 414,857
    * Sedan – 179,118
* Statistics on the number of accidents in each borough.
    * Brooklyn – 349,682
    * Queens – 299,308
    * Manhattan – 272,131
    * Bronx – 156,906
    * Staten Island – 49,526
* Most common accident locations
    * The most common location is in the borough of Manhattan 