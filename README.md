# SMC23_DataChallenge
This data challenge involves analyzing telemetry data from the SUMMIT supercomputer to gain insights into power consumption patterns and system dynamics. The Python scripts provided in this repository process the large-scale Parquet files and generate interactive visualizations for comparative analysis, enabling a deeper understanding of the system's behavior on specific dates.

## Data
The telemetry data is stored in Parquet files. Unfortunately, due to their large size, the Parquet files are not included in this GitHub repository. However, you can obtain the necessary Parquet files from the SUMMIT supercomputer data repository. By modifying the `file_names` list in the scripts, you can analyze other Parquet files associated with the SUMMIT telemetry.

## Program 1: Challenge_3.1.py
The script `Challenge_3.1.py` processes the telemetry data and generates interactive HTML visualizations. It performs the following steps for each file in the `file_names` list:
- Creates DataFrames from the Parquet files and removes duplicate rows.
- Averages values with the same hostname and timestamp.
- Calculates the average temperature of each node and the input power for each timestamp.
- Creates Node Scatter, Node Time Series, and Cabinet Time Series plots for each date.
- Exports the plots as interactive HTML files.

## Program 2: Challenge_3.2.py
The script `Challenge_3.2.py` is designed to perform a more nuanced analysis of the telemetry data. It processes the data for the five specified dates simultaneously and generates five subplots for each type of chart. The visualizations include Power Consumption, Power Magnitude, Power Gradient, Power Spectrum, and Power Spectral Density (PSD) comparisons. These subplots provide a comparative view of the system's power behavior across the five selected dates.

## Instructions
To use the scripts, follow these steps:
1. Obtain the required Parquet files from the SUMMIT supercomputer data repository.
2. Save the Parquet files in the same directory as the Python scripts.
3. Adjust the `file_names` list in the scripts to include the filenames of the Parquet files you want to analyze.
4. Run the scripts using Python, and the visualizations will be generated as interactive HTML files.
5. Open the HTML files in your web browser to explore and analyze the telemetry data.

## Note
Please be aware that processing an incorrect number of Parquet files simultaneously with Program 2 may result in unexpected results. It is recommended to use Program 2 for comparative analysis with of five Parquet files at a time to ensure clarity and ease of interpretation. If it is desired to process more or less Parquet files than five, the code relating to the plotly chart generation will need to be augmented. 

For any inquiries or issues related to this project, feel free to contact the repository owner or author.

---
Author: Joseph Caldwell
Date: 8/1/23
























This repository contains Python programs to process and visualize telemetry data from the SUMMIT supercomputer. The data is stored in Parquet format, but it is not included in this repository due to its large size. However, you can easily analyze your own telemetry data by following the instructions below.

Background
SUMMIT is one of the world's most powerful supercomputers, located at the Oak Ridge National Laboratory in the United States. It is designed for high-performance computing (HPC) and scientific research applications. SUMMIT's massive processing capabilities generate a vast amount of telemetry data, capturing critical information about power consumption and temperature variations within the system.

The challenge presented by this data is to understand and manage the dynamic nature of power consumption in an HPC environment like SUMMIT. By analyzing and visualizing the telemetry data, researchers and administrators can make informed decisions to optimize the system's efficiency and performance.

Requirements
To run the Python programs, you will need the following libraries:

pyarrow
numpy
pandas
plotly
You can install these libraries using pip


Prepare your telemetry data in Parquet format. Please ensure that the Parquet files are compatible with the expected data structure for the programs to work correctly.

Place your Parquet files in the same directory as the Python programs. If your files are too large to be uploaded to GitHub, make sure they are available locally.

Analyzing Telemetry Data
Challenge_3.1: Data Processing and Visualization
The program1.py script processes the telemetry data and generates interactive visualizations of power consumption and temperature fluctuations for specific dates.

To use program1.py, open the script in your preferred Python environment, and modify the file_names list with the names of the Parquet files you want to analyze. You can add or remove file names to process as many files as you like.

Once you have updated the file_names, run the script. The program will process the data and create interactive HTML files for each date specified. These files will contain visualizations of power consumption and temperature fluctuations for individual nodes and cabinets.