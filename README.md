Automatidata Project: NYC Taxi Data Inspection and Analysis
Description
Welcome to the Automatidata Project! This repository contains a Jupyter Notebook that serves as the initial phase of a data consulting engagement for the New York City Taxi and Limousine Commission (NYC TLC). The primary goal of this project is to thoroughly inspect, understand, and prepare a provided dataset of NYC taxi trip data for subsequent analysis, visualization, and hypothesis testing.

This project focuses on ensuring the data is clean, insightful, and ready for advanced analytical activities, identifying key variables, and informing team members of initial findings.

Project Structure & PACE Stages
This project notebook is structured around the PACE (Plan, Analyze, Construct, Execute) problem-solving framework, guiding the data analysis process through distinct stages:

Part 1: Understand the Situation (PACE: Plan)

Focuses on preparing to understand and organize the taxi cab dataset and information.

Part 2: Understand the Data (PACE: Analyze)

Involves creating a pandas DataFrame, performing a cursory inspection (.head(), .info(), .describe()), and compiling summary information.

Part 3: Understand the Variables (PACE: Execute)

Guides deeper investigation into specific variables based on insights from summary data, including sorting and interpreting key columns.

Key Activities & Findings
The notebook guides the user through various data inspection and analysis tasks, revealing initial insights into the dataset:

Data Types and Null Values:

Identified non-numeric data types for datetime columns, which would require conversion for time-series analysis.

Confirmed no null values across the dataset.

Renamed the initial unnamed ID column to 'id' for clarity.

Distribution Analysis (df.describe()):

fare_amount: Noted a wide distribution with a maximum value of $1000, significantly higher than the 25-75 percentile range, and critically, the presence of questionable negative values.

trip_distance: Observed that most rides are between 1-3 miles, with a maximum distance exceeding 33 miles.

Variable Investigation (trip_distance and total_amount sorts):

Confirmed that the longest rides are approximately 33 miles.

Highlighted that the highest total_amount values are significantly larger than others, and negative values exist, warranting further investigation.

Discovered that the most expensive rides are not necessarily the longest ones, indicating other factors influence total fare.

Payment Type Analysis:

Identified the distribution of payment types: Credit Card (15265), Cash (7267), No Charge (121), Dispute (46).

Calculated average tips: Credit card payments had an average tip of ~$2.73, while cash payments had an average tip of $0.00.

Vendor ID Analysis:

Determined the representation of each VendorID: VendorID 2 (12626 trips) and VendorID 1 (10073 trips).

Calculated the mean total_amount for each vendor, showing very similar averages (~$16.30 for VendorID 1 and ~$16.32 for VendorID 2).

Passenger Count & Tip Analysis (Credit Card Payments):

Analyzed passenger counts for credit card payments, with 1 passenger being the most common (10977 trips).

Calculated average tip amounts across different passenger counts for credit card payments, generally ranging from ~$2.60 to ~$2.80.

Technologies Used
Python 3.x

pandas: For data manipulation and DataFrame operations.

numpy: For numerical operations.

Jupyter Notebook: For interactive data exploration and analysis.

Data Source
The project utilizes the 2017_Yellow_Taxi_Trip_Data.csv dataset, which is typically pre-loaded in the lab environment where this notebook is designed to run.

Setup & Usage
To use this project:

Ensure you have Jupyter Notebook installed. If not, you can install it via pip:

pip install notebook

Clone this repository (if it's hosted on GitHub):

git clone https://github.com/your-username/automatidata-taxi-analysis.git
cd automatidata-taxi-analysis

(Replace your-username with your actual GitHub username)

Open the Jupyter Notebook:

jupyter notebook

Navigate to and open the Automatidata_Project_Notebook.ipynb file (or similar name if the notebook has a different name) in your browser.

Run the cells sequentially to follow the data inspection and analysis process. The dataset is typically pre-loaded in the lab environment, so no separate download steps are usually required for the CSV data.

Project Structure
automatidata-taxi-analysis/
├── Automatidata_Project_Notebook.ipynb
├── README.md
├── requirements.txt
└── (potentially: 2017_Yellow_Taxi_Trip_Data.csv - if not pre-loaded)

Supporting Files
Automatidata_Project_Notebook.ipynb
This is the main Jupyter Notebook file containing all the code, analysis, and questions for the project.

requirements.txt
This file lists the Python libraries required to run the notebook.

pandas
numpy

License
This project is licensed under the MIT License. See the LICENSE file for details.

Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.
