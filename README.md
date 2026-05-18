Production-ready end-to-end medallion architecture pipeline on Databricks incrementally processing dummy financial and user data for a biotech company.
<img width="1810" height="1040" alt="image" src="https://github.com/user-attachments/assets/1636dbca-feaf-4ac5-b992-b09b7f8b9b04" />

<details> 
<summary><strong>Dashboard Images</strong></summary>
 
<img width="2857" height="1442" alt="image" src="https://github.com/user-attachments/assets/3da270ed-0d1d-4e63-ab6a-b45cea1176e6" />
<img width="2875" height="1315" alt="image" src="https://github.com/user-attachments/assets/c3eba572-b7f4-4ded-852d-c1cc19d076d8" />
<img width="2852" height="1380" alt="image" src="https://github.com/user-attachments/assets/853af8b4-d776-4d33-b3cd-ff085272bbe1" />

</details>

<details> 
<summary><strong>Databricks Job images</strong></summary>
*Master Main Databricks Job: runs all the smaller jobs when data is available in source
<img width="1707" height="525" alt="image" src="https://github.com/user-attachments/assets/197a8720-0d05-46b0-ace5-112638dc7233" />

\
*Source to Silver Databricks Job: ingest data from source(S3, Azure) to Bronze then silver layer
<img width="1690" height="580" alt="image" src="https://github.com/user-attachments/assets/c4e3829b-4033-49a0-bd7e-7af89726f7cf" />

\
*Silver to Gold Databricks Job: combines data from silver tables and puts it in Gold layer 
<img width="1395" height="355" alt="image" src="https://github.com/user-attachments/assets/74046a88-37f6-462a-90ea-123f9ff868c1" />

</details>

<details> 
<summary><strong>Data Model</strong></summary>
 
  <details> 
  <summary><strong>    Bronze and Silver layer</strong></summary> 
  <img width="2010" height="1160" alt="image" src="https://github.com/user-attachments/assets/e3126b55-7077-4a68-a4b2-4b33da02c905" />
  </details> 

  <details> 
  <summary><strong>    Gold layer</strong></summary> 
  <img width="1960" height="1117" alt="image" src="https://github.com/user-attachments/assets/ee07bf50-f622-434c-8130-89484c6c700b" />
  </details>  

</details>


<details> 
<summary><strong>E-Mail Alerts</strong></summary>
<img width="1737" height="945" alt="image" src="https://github.com/user-attachments/assets/cb848d24-41d3-41d3-9b6a-e866e2175199" />
</details>
 
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

This project is a production-ready end-to-end pipeline on Databricks. It ingests financial and consumer data to be processed into a medallion architecture pipeline to then be displayed on dashboards on databricks for end users to analyze and run AI agents on. 

**Ingestion**

Raw Data is ingested into a bronze layer where it's cleaned up and passed to a silver layer and finally aggregated and joined in the gold layer where queries will run on top to feed various dashboards.

It ingests data from two different sources(AWS S3 and SQL Server on Azure). It uses a JDBC connection to ingest data from SQL Server and uses Autoloader on Databricks to ingest data from S3.

**Orchestration**

The pipeline is ran by PySpark Notebooks. Those notebooks are ran/scheduled by Databricks jobs with the help of tables(tables, table_parameters, table_watermarks, pipeline_runs) containing metadata about each main table and their previous runs.

**Presentation**

Once the data is aggregated and pushed to the dashboards end users can interact with the data and even use Databricks built-in AI agent(Ginie) 
to query, analyze, and visualize the data without writing code. 
</details>

<details> 
<summary><strong>Features</strong></summary>

+ Displays multiple tables and charts showing KPIs, metrics and other critical data in an interactive way.
+ Use AI agents to query, analyze, and visualize without writing code.
+ Sends e-mail alerts when pipeline fails or succeeds along with pipeline run metrics.

</details>
