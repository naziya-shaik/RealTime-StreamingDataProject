# Real-Time Data Streaming using Apache Nifi, AWS, Snowpipe, Stream & Task:

** project Overview:**

	The "Real-Time Data Streaming" project is a sophisticated solution designed to streamline the continuous flow and processing of data in real-time. Combining innovative technologies such as Faker, Docker, Apache NiFi, Zookeeper, AWS, Snowpipe, Stream, and incorporating Slowly Changing Dimensions (SCD) strategies (SCD1 and SCD2), this project addresses the need for efficient, scalable, and dynamic data streaming architectures.
 
**1.Faker:**
The Faker library in Python is utilized to generate realistic, synthetic data. The library allows you to create random data such as names, addresses, email addresses, street, and much more information about customer. 

**2. Docker:**
Docker containers play a crucial role in encapsulating and deploying various project components. This approach enhances portability, scalability, and consistency across different environments.
	Docker is a platform and a set of tools designed to facilitate the creation, deployment, and execution of applications within lightweight, portable, and self-sufficient containers.
 
#3. Apache NiFi:
•	Apache NiFi serves as the central platform for designing and orchestrating data flows between EC2 instance and AWS S3 bucket. With its user-friendly interface, NiFi facilitates the integration, transformation, and routing of both real and synthetic data in real-time.
•	Processors handle the ingestion, transformation, routing, and interaction with data as it moves through the NiFi data flow. This process created three processors those are:
a)	List file:
b)	Fetch File:
c)	PutS3Object:
•	They provide a wide range of functionalities for handling data from diverse sources, transforming it, and efficiently routing it to various destinations in the data ecosystem. By running the processors customer file will be automatically loaded into AWS S3 bucket.

#4.Zookeeper:
•	Apache Zookeeper is employed for distributed coordination and synchronization. It ensures the reliability and fault-tolerance of the system, providing centralized configuration management for a dynamic and scalable architecture.
#5.Docker Compose:
•	Docker Compose is a tool for defining and running multi-container Docker applications. 
•	By using Docker Compose Jupyter, Apache Nifi, Zookeeper used together. Making it easy to manage complex deployments and services.
#6. Snowpipe:
•	Snowpipe is integrated to automate the loading of streaming customer data into Snowflake, a cloud data warehouse. This ensures continuous updates to the data warehouse, making the latest customer data available for analysis.
•	By using IAM credentials created External Stage and copy the data into customer raw table. 
#7.Snowflake Stream:
•	Snowflake provides a feature called Change Tracking that allows you to track changes to a table. This is sometimes referred to as a "stream" in a more general sense. Change tracking enables you to identify rows that have been inserted, updated, or deleted (DML commands) since the last time the stream was consumed.
•	Any changes to customer data in real time will be captured automatically.

#8.Target Table1 & Target Table2:
    a)Slowly Changing Dimension Type 1 (SCD1):
Specifically, SCD1 addresses the customer data overwritten with new values. In SCD1, when a change occurs in a dimension attribute, the existing record is updated with the new values, effectively overwriting the previous state. This means that only the latest version of the data is retained into the Actual table.
    b) Slowly Changing Dimension Type 2 (SCD2):
SCD2 maintains a historical record of changes by creating new records with updated information. This allows for the tracking of historical data and analysis of how data evolve over time.
The inclusion of SCD1 and SCD2 strategies accommodates changes in both synthetic and authentic data, offering flexibility and accuracy in tracking real-time updates and historical changes.




![streaming-data](https://github.com/naziya-shaik/RealTime-StreamingDataProject/assets/111407441/b66b1f35-f762-45e7-8c5a-9eaec49ad089)
