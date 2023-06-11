# StackOverflow User Behavior Analysis

## Overview
A data analysis project aimed at extracting insights from StackOverflow user data. \
This analysis focuses on determining programming language usage, identifying active users and posts, and identifying the most shown-up websites. \
By leveraging **Apache Spark**'s distributed computing capabilities, the analysis efficiently processes large volumes of data to uncover valuable insights.

**Technical features** in this analysis:
|Features| Description |
|:------|-----------:|
|**DBMS**|MongoDB|
|**Distributed Data Processing**|Utilizes Apache Spark for distributed data processing, enabling efficient analysis of large datasets|
||PySpark, Spark's DataFrame API for data manipulation, aggregation, and analysis|
|**Large Data Source**|GBs|
|**Data cleaning and transformation**|Applies Regex-based filtering techniques to identify programming languages, active users, and active posts|
|**Interactive Computing Platform**|Jupyter Notebook: flexible interface allows users to configure and arrange workflows in data science, and scientific computing|


#### Explode the repository 
|Files| Description |
|:------|-----------:|
|what-how-why.txt|Analysis document|
|spark-defaults.conf|Spark config files for needed packages|
|analysing-SOF-users.ipynb|Source code for analysis and explanation|
|.data-source/demo|Demo data|
|.data-source/fulldata.txt|Full data|

## Clone the data warehouse
#### Requirements and Setup Apache Spark
1. Install Apache Spark by following the official documentation: [Apache Spark Installation](https://spark.apache.org/docs/latest/index.html).
2. Set up a Spark cluster or standalone mode according to your requirements.
3. Ensure that the Spark cluster has sufficient resources to handle the data size and computational demands of the analysis.

#### Requirements and Setup MongoDB
1. Install MongoDB by following the official documentation: [MongoDB Installation](https://docs.mongodb.com/manual/installation/).
2. Set up a MongoDB instance and ensure it is accessible from your Spark environment.
3. Import the StackOverflow user data into MongoDB and store it in a suitable format for analysis (e.g., HTML responses).

#### Requirements and Setup Python and Jupyter Notebook
1. Install Python, if not already installed, by following the official Python documentation: [Python Installation](https://www.python.org/downloads/).
2. Install Jupyter Notebook by following the official Jupyter documentation: [Jupyter Notebook Installation](https://jupyter.org/install).
3. Install the findspark module by running the following command:
```cli
pip install findspark
```

## Running the Analysis
1. Set up the necessary dependencies and environment for your Jupyter Notebook project.
2. Configure the Spark cluster or standalone mode in the code, adjusting the settings according to your setup.
3. Update the code to match your MongoDB connection details, including the host, port, and database name.
4. You will need to install MongDB jar package within Spark engine for interaction, one simple way is clone the`spark-defaults.conf` to `[your path]/apache-spark/[your version]/libexec/conf` for installation.
4. Modify the Regex patterns in the code to match the structure and format of your HTML data.
5. Import the findspark module in your Jupyter Notebook using the following code:
```python
import findspark
os.environ["JAVA_HOME"] = "[your path]/openjdk@11/[your version]"
os.environ["SPARK_HOME"] = "[your path]/apache-spark/[your version]/libexec"
findspark.init()
```
6. Run the analysis code cells in the notebook to perform the StackOverflow user behavior analysis.
7. Review the generated visualizations and reports to gain insights into StackOverflow user behavior.
