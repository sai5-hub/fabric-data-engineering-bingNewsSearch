# **Bing News Search — An End-to-End Azure Data Engineering Project in Microsoft Fabric**

## **🌟 Overview**

Utilizing the Bing News API within Azure, the project builds a comprehensive end-to-end Data Engineering solution using Microsoft Fabric. The goal is to analyze the latest news, determine the sentiment of each news item, and create interactive dashboards that effectively visualize the insights.

To break it down, this project involves six key steps:

1.	Create a Bing Search Resource in Azure
2.	Data Ingestion
3.	Data Transformation with Incremental Loading
4.	Sentiment Analysis with Incremental Loading
5.	Data Visualization and Reporting in Power BI
6.	Set up Alerts with Data Activator with notifications on Teams/Email

A step by step guide to run this pipeline

https://medium.com/@thondapu.sai5/bing-news-search-an-end-to-end-azure-data-engineering-project-in-microsoft-fabric-298012488165

## **Why This Project?**

Real-World Application: Extracting valuable insights from news data using AI-driven sentiment analysis.

Comprehensive Tech Stack: Covers API data ingestion, cloud storage, distributed computing, data transformation, and reporting.

Hands-On Learning: Integrates key Azure services with Fabric to handle structured and unstructured data efficiently.

🔑 Key Features & Learnings

Accessing and ingesting news data from Bing API

Processing and transforming news data using Spark

Storing data efficiently in Delta Lake for optimized querying

Performing sentiment analysis using Text Analytics

Visualizing news trends and insights with Power BI

Implementing incremental data loading and real-time alerts with Data Activator

![Screenshot (419)](https://github.com/user-attachments/assets/a414ca11-89d6-44f2-9a01-7ff3b1df2cbe)





## **Technical Skills**



## **Data Source**
Bing latest news data was loaded from Bing Search Resource News Search APIs v7 (https://api.bing.microsoft.com/v7.0/news/search) available in Azure.


## **Approach**
1. Create a Bing Search Resource in Azure:
I created rg-bing-data-analytics resource group in Azure Subscription 1, and used the marketplace to search for the Bing Search v7 API to create a Bing Search resource. Selected F1 free tier with 1,000 monthly calls.

2. Data Ingestion:
As our data lake, I created a Microsoft Fabric Lakehouse called the bing_olympic_news_db which I connected the Bing Search resource API and also configured the Source and Destination.

Configuring the Data Source  To connect to the source data, I use the RestAPI connection available in Fabric to connect to the Bing Search resource API in Azure.
Setting the Data Destination. For the Destination, I set the destination to the bing_olympic_news_db Lakehouse I had created earlier. I also created a file path called olympic-news.json and set the file format to JSON.

3. Data Transformation with Incremental Loading:
I use the spark job within Microsoft Fabric for this and I also implement a Type 1 SCD to load our data into the Lakehouse incrementally.

4. Sentiment Analysis with Incremental Loading:
For the Sentiment Analysis, I use SynapseML formerly (MMLSpark) which is an open-source library that is available within Microsoft Fabric. It is a pre-built intelligent model for our machine learning task and predicts the Olympic news sentiments based on the news description column which has a detailed description of the news article as seen above.

5. Schedule Refresh:
Since the news data is live, there is a need to schedule its refresh every morning at 7 am in Data Factory. This refresh covers the data Ingestion (pipeline), ETL_process_olympic_news (notebook), and olympic_news_sentiment_analysis.ipynb (notebook) The refresh schedule is shown here 👇

6. Data Visualization in Power BI:
Below is the Data Visualization and report of the Olympic news for the past 7 days as at when I performed this analysis. Over 100 news was published and only 17% of it has positive sentiments.

7. Set up Alerts with Data Activator with notifications on Microsoft Teams:
I created an alert called Positive Alert Item and I would like to receive a Teams message alert when the Positive Sentiment is greater than 17%.
