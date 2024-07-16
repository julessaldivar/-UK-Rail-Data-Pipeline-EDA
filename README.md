# Evaluating the Accessibility, Convenience, and Reliability of the UK Railway System

**Authors**: Jules Saldivar and Audrey Warner

**Instructor**: James Meredith

**Institution**: Grand Circus Bootcamp

Active Project Dates: 7/3/24 - 7/17/24 
![image](https://github.com/user-attachments/assets/6bdd30e2-71a0-4540-9d6d-d5fc67f64449)

### How We Got Our Data

#### Overview

As part of the Data Analytics & Engineering with Python course, our group project analyzed the accessibility, convenience, and reliability of the UK Railway System. The project involved setting up a data pipeline to pull live data from the UK Open Rail Data API, transforming the data using Docker, Kafka, and Spark, and loading it into a PostgreSQL database for analysis. This section details the steps we took to set up our data pipeline and perform exploratory data analysis (EDA) on the collected data.

#### Data Pipeline Setup

**1. Data Collection:**
- **UK Open Rail Data API:** We collected real-time data on train schedules, actual arrival and departure times, delay statuses, and station information.
- **Rail References Data:** This dataset was merged with the API data to provide additional insights, fill in station names, and find related coordinates for mapping. 
- **2021 UK Census Population Data:** Used to correlate train station locations with populous areas.

**2. Pipeline Components:**
- **Kafka Producer:** Connects to the UK Open Rail Data API, processes messages, and forwards the processed data to a Kafka topic.
- **Kafka Consumer:** Listens for messages from the Kafka producer, processes the data, and loads it into a PostgreSQL database.
- **PostgreSQL Database:** Hosted on AWS, stores the processed data for further analysis.

**3. Technologies Used:**
- **Docker:** Containerizes our data pipeline components.
- **Kafka:** Enables real-time data streaming.
- **Spark:** Handles data transformation and processing.
- **AWS:** Hosts our PostgreSQL database.

#### Exploratory Data Analysis (EDA)

**1. Data Preparation:**
- **Loading Data:** Used Jupyter notebooks to connect to our PostgreSQL database and load the collected data.

**2. EDA Phases:**
- **Data Cleaning:** Ensured consistency and accuracy for analysis.
- **Data Merging:** Merged the Station Rail Name Reference Table with the API data.
- **Data Analysis:** Explored train delays, station busyness, and travel patterns. Focused on identifying the top 10 most frequently visited stations and the busiest times at certain stations.

**3. Insights and Visualizations:**
- **Accessibility:** Analyzed the distribution of train stations in relation to population density.
  ![image](https://github.com/user-attachments/assets/ecbc86b4-ffc8-4aa0-abd4-745e24d084e8)
  ![image](https://github.com/user-attachments/assets/c7ad27ba-7ba2-41c3-ad29-1d754f757b83)

- **Convenience:** Examined train schedules to determine availability at different times.
- **Reliability:** Investigated train delays and evaluated overall reliability.

### Analysis of Findings: Accessibility, Convenience, and Reliability of the UK Railway System

#### Accessibility

**1. Distribution of Train Stations:**
- High density of train stations in densely populated areas like London, Birmingham, Manchester, and Glasgow.
- 19 out of the top 20 stations are located in London.
- Stations are predominantly located in metropolitan areas, making the system highly accessible.

**Conclusion:** The UK railway system is accessible, especially in metropolitan areas where stations are numerous.

#### Convenience

**2. Train Schedules:**
- Majority of trains operate between 1:00 PM and 9:00 PM, ensuring convenience for daytime travelers.
- Lack of trains running between 1:30 AM and 4:30 AM, which might inconvenience late-night travelers.
- Weekday train availability is high; additional analysis on weekend schedules would provide more insights.

**Conclusion:** The UK railway system is convenient for most daytime travelers but less so for late-night travel.

#### Reliability

**3. Delays and Punctuality:**
- 13.32% of all trains are delayed, with 75% of delays exceeding 5.5 minutes.
- Trains scheduled to arrive earlier than 5:00 AM are 25% more likely to be delayed.
- Despite more evening trains, delays do not increase proportionally, indicating consistent reliability issues.

**Conclusion:** The UK railway system struggles with reliability due to significant delays.

### Summary of Findings

- **Accessible:** Well-connected in densely populated areas.
- **Convenient:** Convenient for daytime travel but less so for late-night.
- **Reliable:** Faces significant reliability challenges with frequent delays.

### Recommendations

**1. Expand Data Collection Period:**
- Extending the data collection period would provide a more comprehensive understanding of the system's performance over time.

**2. Evaluate Cost and Safety:**
- Including analyses on cost and safety would offer travelers a more holistic view of the service.

**3. Compare Alternative Travel Options:**
- Comparing with other forms of transportation (e.g., car, air, bus) could help travelers make more informed decisions.

**4. Address Reliability Issues:**
- Implementing measures to reduce delays and improve punctuality should be a priority to enhance reliability.

By addressing these areas, the UK railway system can improve its accessibility, convenience, and reliability, ultimately providing a better travel experience for all users.

## For More Information

For any additional questions, please contact Jules Saldivar at <julessaldivar@gmail.com>, or on [LinkedIn](https://www.linkedin.com/in/jules-saldivar/) or Audrey Warner at <audrey.warner1@outlook.com>, or on [LinkedIn](https://www.linkedin.com/in/audrey-warner-data1/).

