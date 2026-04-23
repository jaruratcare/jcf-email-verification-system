# JCF Email Verification System

## Overview
This repository contains the Java-based email verification microservice and the associated Python bulk filtering tool. It is designed to rapidly process and validate large batches of email addresses without relying on traditional SMTP handshakes.

## Setup Instructions

### 1. Java Installation and Configuration
* **Install Java 21:** Download Java 21 from Eclipse Temurin at https://adoptium.net/temurin/releases/?version=21.
* **Configure Environment:** Add the extracted Java installation path to your system's PATH environment variable.
* **Verify Installation:** Open your command prompt (cmd) and run the command `java -version` to ensure Java is visible and correctly installed on your machine.

### 2. Repository Setup
* **Clone the Repository:** Clone this project to your local machine using Git and navigate into the project directory.

### 3. Data Preparation
Navigate to the Python bulk filter folder and add your input file. You must strictly follow these three precautions:
1. **Source Format:** Make sure the output format is exactly the same as the one provided by the JCF email scraper service.
2. **No Headers:** Make sure that there are no headers in the file. The file should be completely raw data as it is.
3. **Exact Naming:** Make sure that the file name is exactly **team_data.csv** without any typos.

### 4. Execution Steps
* **Start the Microservice:** Run the Java Spring Boot microservice. Check your console logs to make sure Tomcat is actively listening on port 8080.
* **Run the Python Filter:** Open your command prompt, navigate to the Python service folder using the `cd` command, and run the following command:
  `python bulk_verifier.py`
  
*(Note: Both dead and valid emails will get automatically saved in separate CSV files in a fraction of the time.)*

## Demo Video
For a complete visual walkthrough of the setup and execution process, please view the demo run here:
https://youtu.be/_WAqMtLg3dE
