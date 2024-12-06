# Analiza-Danych-Pandas-Pawel-Kossowski

## Table of Contents
* [General Info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)

## General Info

The project involves analyzing data from the nypd-motor-vehicle-collisions.csv dataset to examine motor vehicle accidents in New York City. The analysis includes data ingestion, cleaning, transformation, and visualization of results. Key aspects include identifying the most dangerous accident factors by borough, determining fatalities and injuries caused by speeding, analyzing the three most common accident causes (both citywide and by borough), identifying the types of vehicles most frequently involved in accidents, and providing accident statistics for each borough. Optionally, the project may include identifying the most frequent accident locations. Findings will be presented with visualizations, along with conclusions.

## Technologies

## Setup

First install in your console the following packages:

``` bash
pip intall kagglehub 
```

Inport the dataset into your directory 

```
import kagglehub
import os
import shutil

# Get the directory of the current script
current_directory = os.path.dirname(os.path.abspath(__file__))

# Download the dataset to the default directory
path = kagglehub.dataset_download("new-york-city/nypd-motor-vehicle-collisions")

# Move the downloaded files to the same directory as the script
if os.path.exists(path):
    for file_name in os.listdir(path):
        source_path = os.path.join(path, file_name)
        target_path = os.path.join(current_directory, file_name)
        shutil.move(source_path, target_path)
```
