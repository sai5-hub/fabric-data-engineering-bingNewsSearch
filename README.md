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

![Medium Article](https://medium.com/@thondapu.sai5/bing-news-search-an-end-to-end-azure-data-engineering-project-in-microsoft-fabric-298012488165)

## **💡 Why This Project?**

**Real-World Application:** Extracting valuable insights from news data using AI-driven sentiment analysis.

**Comprehensive Tech Stack:** Covers API data ingestion, cloud storage, distributed computing, data transformation, and reporting.

**Hands-On Learning:** Integrates key Azure services with Fabric to handle structured and unstructured data efficiently.

## **Architecture**

![Screenshot (419)](https://github.com/user-attachments/assets/a414ca11-89d6-44f2-9a01-7ff3b1df2cbe)

## **🔑 Key Features & Learnings**

* Accessing and ingesting news data from Bing API
* Processing and transforming news data using Spark
* Storing data efficiently in Delta Lake for optimized querying
* Performing sentiment analysis using Text Analytics
* Visualizing news trends and insights with Power BI
* Implementing incremental data loading and real-time alerts with Data Activator

## **🛠 Technologies, Tools, and Frameworks**

* Azure Data Factory - ETL pipeline automation
* OneLake & Delta Lake - Scalable data storage
* Synapse Data Engineering - Data transformation
* Text Analytics - Sentiment analysis
* Power BI - Data visualization
* Data Activator - Real-time notifications
* Spark Notebooks - Interactive analysis

## **🚀 Data Source**
Bing latest news data was loaded from Bing Search Resource News Search APIs v7 (https://api.bing.microsoft.com/v7.0/news/search) available in Azure.

## **🛠 Installation & Usage**

Follow these steps to set up and run the project locally or in the cloud.

**Prerequisites**

* Azure Subscription with access to Fabric services.
* Bing News Search API Key (F1 Free Tier recommended for testing).
* Basic understanding of Python, SQL, and Spark.

**Quick Start**

* Clone this repository.
* Set up an Azure resource group and provision Bing Search v7 API.
* Configure Data Factory and Synapse to ingest and process data.
* Execute sentiment classification on ingested news.
* Use Power BI to explore and visualize trends in the news dataset.
* Enable Data Activator for real-time alerts.

1. Clone the repository
2. Set up Azure resources:
* Create a Resource Group in Azure.
* Deploy Bing Search v7 API in Azure Marketplace.
* Set up OneLake storage.
3. Configure Spark Notebooks & ADF Pipelines:
* Import provided Spark Notebooks into Synapse.
* Set up ADF Pipelines for automated ingestion.
4. Run Sentiment Analysis:
* Configure Azure Cognitive Services API.
* Execute sentiment classification on ingested news.
5. Visualize in Power BI:
* Connect Power BI to OneLake.
* Build interactive reports and dashboards.
6. Enable Data Activator for real-time alerts.
  
## **📚 Resources & Further Reading**

* Microsoft Fabric Documentation: ![Learn More](https://learn.microsoft.com/en-us/fabric/)
* Azure Cognitive Services: ![Text Analytics API](https://learn.microsoft.com/en-us/azure/ai-services/language-service/)
* Medium Blog Post: ![Step-by-Step Guide](https://medium.com/@thondapu.sai5/bing-news-search-an-end-to-end-azure-data-engineering-project-in-microsoft-fabric-298012488165)





