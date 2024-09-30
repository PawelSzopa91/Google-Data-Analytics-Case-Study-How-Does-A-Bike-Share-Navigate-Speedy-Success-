# Google Data Analytics Case Study How Does A Bike Share Navigate Speedy Success
Case Study from Google Data Analytics Certification
## Introduction
This case study is part of the capstone project for the Google Data Analytics course on Coursera. The task involves using available data to gain fresh insights, make data-driven choices, and solve business challenges. The scenario focuses on Cyclistic, a fictional bike-sharing company based in Chicago.

In 2016, Cyclistic introduced a successful bike-sharing service. Since its launch, the program has expanded to include 5,824 bicycles, all equipped with GPS and locked into a network of 692 stations across Chicago. Riders can pick up a bike at one station and return it to any other station in the system at any time.

The marketing department believes that the company's long-term growth relies on increasing the number of annual memberships. Therefore, the goal of my team of marketing analysts is to examine how casual users and annual members use the bikes differently. The insights gained from this analysis will help in developing a new marketing strategy aimed at converting casual riders into annual members.

## Gathering and Describing the Data
Google provided a link to Cyclistic's dataset, which spans back to 2013. However, following the instructions, I only focused on the most recent 12 months, from August 2020 to July 2021. Although the data comes in CSV format, the files are quite large—July 2021 alone is around 150 MB. To manage this data, I used the R programming language for inspection.

![tabale 1](https://github.com/user-attachments/assets/6991ca73-381b-4c47-9d87-44e61232b08d)
Dataset in R Studio

![table 2](https://github.com/user-attachments/assets/a486e4af-e5d8-4007-8d81-fb8d843e0648)

The image above shows the data from August 2020 after being imported into R Studio. This dataset records the trip histories of Cyclistic's customers, including trip ID, bike type, rental and return times, rental and return locations, and customer types. I noticed there were redundant variables and some missing (NA) values in the dataset.

## Data Processing
Based on the dataset, I hypothesized that the key difference between annual members and casual users would lie in their trip duration and the number of trips they take over time. Therefore, I began by cleaning the raw data, retaining only the necessary variables such as ride ID, bike type, rental and return times, and customer type. I also wrote simple R scripts to calculate the duration of each trip and determine the day of the week on which each trip started.

![table 3](https://github.com/user-attachments/assets/5b494ca0-4e86-4573-a661-1bb32fd68786)

Cleaning the dataset significantly improved its readability and reduced its file size. I removed rows with NA values, discarded station details, and filtered out trips shorter than 60 seconds. Trip durations were calculated in seconds, allowing for more flexibility in future analysis.

## Data Analysis
From my initial prediction, I refined the focus into several key questions:

### 1. What are the differences in the average trip duration between annual members and casual riders?

### 2. Is there a relationship between trip duration and the day of the week? If so, how does this differ between customer types?

### 3. How do the number of trips taken by each customer type vary?
I performed some basic data aggregations to start answering these questions:

Average Trip Duration

![table 4](https://github.com/user-attachments/assets/127e7f0d-ae13-49ce-853b-1b7636f340cc)

In August 2020, casual riders took trips that were roughly three times longer than those of annual members. Interestingly, the longest trip duration for both groups approached one month, suggesting that some users may have forgotten to return the bikes
When we zoom in to the specific weekdays, there is certainly a pattern:

![tab 1 1](https://github.com/user-attachments/assets/39197950-4dfd-4f8f-9e84-cadbadc6835d)

Annual members completed more trips overall compared to casual riders. This suggests that those with an annual membership are likely to use the bikes more frequently, potentially for commuting or for other economic, social, or environmental

![1 3](https://github.com/user-attachments/assets/99a4dc56-a30b-4e53-8858-9b2fd6eb1c24)

When analyzing the number of trips by day of the week, annual members maintained a steady number of rides throughout the week. In contrast, casual riders showed a more uneven distribution, with far more trips taken on weekends than weekdays. This supports the hypothesis that annual members view bikes as a primary mode of transportation, while casual riders may use them more for leisure.

## Number of trip
![1 2](https://github.com/user-attachments/assets/eb9418b7-c742-40f5-95f3-fb51a7d16c07)

However, this analysis is somewhat limited by the fact that the dataset doesn't include the actual number of annual members or casual riders. A more accurate picture could be drawn from an analysis that considers the number of users per group.

# Visualizing Data for the Entire Year

![100](https://github.com/user-attachments/assets/8c59aa93-d58e-4493-9b2b-65b4e39eeee1)

After analyzing data for August 2020, I imported all monthly datasets into Tableau to generate a broader view of the entire year. The first chart shows average trip durations, while the second visualizes the number of trips taken by annual members and casual riders.

![200](https://github.com/user-attachments/assets/0004fe19-cf26-4f74-a9c5-0cd091676ab9)

The charts reveal that casual riders consistently took trips that were two to three times longer than those of annual members. Annual members, however, had stable trip durations throughout the year, while casual users experienced more variation. Both groups followed a similar pattern regarding day of the week, with longer rides occurring on weekends.

Annual members made more trips overall, especially when compared to casual riders, mirroring the results from August 2020. The data suggests that the service sees its highest usage in the middle of the year, with a significant drop-off between December and January. In terms of trips per day, annual members maintained a consistent count throughout the week, while casual riders favored weekends for their rides.

Another interesting insight is the number of trips taken by the hour. Bikes are rented at all hours of the day, even between midnight and dawn, with 4 AM being the quietest time. For annual members, trip numbers peaked around 8 AM, noon, and 5 PM, likely corresponding to commutes or meal breaks. For casual riders, 5 PM marked the busiest time of day for trips.

# Final Conclusion and Recommendations

From my analysis and data visualization, I was able to draw some conclusions about how casual riders and annual members use Cyclistic's bike-sharing service differently.

A key characteristic of annual members is their consistent and frequent usage, both in terms of trip count and duration. This suggests that they rely on bikes for practical purposes, such as commuting or addressing environmental, cost, or convenience factors. On the other hand, casual riders don’t use the bikes as regularly, likely because they don't need them for everyday activities. When they do use the bikes, they tend to take longer, leisurely rides on weekends.

In conclusion, the differences between the two groups seem to stem from how they perceive and utilize the bike-sharing service, with annual members integrating it into their routines and casual riders using it more sporadically.

Based on these findings, I would suggest three recommendations for the marketing team to convert casual riders into annual members:

### 1. Emphasize the benefits of biking as a regular mode of transportation, especially highlighting the personal advantages for casual riders, such as health, convenience, and cost savings.

### 2. Enhance the annual membership package by adding more perks like discounts, exclusive features, or access to special events or communities for bikers.

### 3. Focus on social media marketing to engage with users. Since most people spend a lot of time on platforms like Facebook, YouTube, and TikTok, building a community there, along with hosting offline events for members, could be very effective. Collaborating with influencers could also help boost the visibility of the service.
