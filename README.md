Production-ready end-to-end medallion architecture pipeline on Databricks processing dummy financial and user data for bio tech company.
<img width="1810" height="1040" alt="image" src="https://github.com/user-attachments/assets/1636dbca-feaf-4ac5-b992-b09b7f8b9b04" />

<details> 
<summary><strong>Technologies</strong></summary>
 
+ PySpark
+ SQL
+ Databricks AI agent 
+ Delta Lake 
+ AWS S3 
+ SQL Server 
+ JDBC
 
</details>

<details> 
<summary><strong>About the project</strong></summary>

This project is a production-ready end-to-end pipeline on Databricks. It ingests financial and cosumer data to be processed into a medallion architecture pipeline to then be displayed 
on a dashboard on databricks for end users to analyze. 

Raw Data is ingested into a bronze layer then cleaned up and passed to a silver layer and finally aggregated and joined in the gold layer where queries will run on that feed to various dashboards.

It ingests data from two different sources(AWS S3 and SQL Server on Azure). It uses a JDBC connection to ingest data from SQL Server and uses Autoloader on Databricks to ingest data from S3.

The pipeline is ran by PySpark Notebooks. Those notebooks are ran by Databricks jobs with the help of metadata about each table and last runs of those tables.

Once the data is aggregated and pushed to the dashboards end users can interact with the data and even use Databricks built-in AI agent(Ginie) 
to query, analyze, and visualize structured and unstructured data without writing code. 

</details>

<details> 
<summary><strong>Features</strong></summary>

+ Displays multiple tables and charts showing KPIs, metrics and other critical data in an interactive way.
+ Use AI agents to query, analyze, and visualize without writing code.

</details>
