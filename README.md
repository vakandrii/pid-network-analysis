# PID network analysis

The goal of this project is to conduct a network analysis of Prague Integrated Transport (PID) stops using open data from 
the Prague Integrated Transport system. By leveraging the General Transit Feed Specification (GTFS) data on transit 
schedules, the project aims to:

- Build and analyze a network of PID stops, treating stops as nodes and connections between consecutive stops on transit 
routes as directed edges.
- Utilize stop attributes such as geographical coordinates for enhanced analysis and graph layout.
- Visualize the PID network, highlighting relevant substructures for readability.
- Apply centrality measures to assess the importance of stops within the network over a weekly period (Monday to Sunday) 
and interpret these measures based on the specific dataset.
- Address custom analytical questions related to stop importance, operational patterns, and accessibility features within 
the PID network.

## Dataset Overview

The dataset will be [Prague Integrated Transport Open Data](https://pid.cz/o-systemu/opendata/). Specifically, we will 
work with [timetable data](https://pid.cz/o-systemu/opendata/#h-gtfs), which is originally in GTFS (General Transit Feed 
Specification) format. This is a format that is used by a wide range of software applications and because of this it is 
also used by public transport agencies, including PID, when publishing data. We constructed the dataset $D$ from data that 
comes from [timetables](https://pid.cz/o-systemu/opendata/#h-gtfs). More information about all the files and their 
attributes can be found in the [GTFS format documentation](https://developers.google.com/transit/gtfs/reference).

* In the `stops.txt` file, the **latitude and longitude** is given for each stop. We can use this data to extend our 
analysis and it can also help us with graph layout.

## Project Structure
The project is organized as follows:
- `d.csv`: Dataset in csv format
- `README.md`: This file providing an overview of the project (You are reading it right now!).
- `pid_analysis.ipynb`: Jupyter Notebook containing the code for preprocessing the dataset, addressing time attributes, 
                        creating and analyzing the PID network representation and exploring custom analytical questions 
                        related to PID stop characteristics.
- `requirements.txt`: List of Python packages required to run the notebook.

## Setup and Usage
1. **Setup**
   - Clone this repository to your local machine.
      ```bash
      git clone https://github.com/vakandrii/pid-network-analysis.git
      ```
   - Navigate to the project directory.
   - Install the required Python packages using pip:
     ```bash
     pip install -r requirements.txt
     ```
   - Launch Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - Open `pid_analysis.ipynb` in your browser.

## Acknowledgment
I extend my sincere thanks to the Prague Integrated Transport system for providing the open dataset necessary for this 
network analysis project. The availability of this data enables valuable insights into public transportation networks. 
Thank you!