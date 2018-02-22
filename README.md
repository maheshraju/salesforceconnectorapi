# salesforceconnectorapi

Salesforce Connector API using MuleSoft
•	I created a RAML specification using the Anypoint Studio to design the REST APIs and then created Mule Flows using the RAML Specification.
•	All the configurations are externalized using properties files (mule-app.properties, http.properties, salesforce.properties)
•	Global Configurations are a part of globalconfigurations.xml, which can be reused across various Mule flows in the application.
•	Dataweave is used to transform the data retrieved from Salesforce into CSV
•	A file component creates a file using the inputs from the Dataweave

Getting Started
•	Import the project into MuleSoft Anypoint Studio
•	Change the salesforce.properties to use valid salesforce login credentials
•	Change the FILE_PATH in mule-app.properties

Prerequisites
•	Mulesoft Anypoint Studio EE ( I used 6.4.2)
•	Java (I used Java 8)

Running
•	There are two main APIs as described below that retrieve Account details from Salesforce using the MuleSoft Salesforce Connector
•	API can be accessed at http://<hostName>:<port>/salesforce/getAllAccounts and 
•	http://<hostName>:<port>/salesforce/getAccountByName?name=xyz
•	Default Values for host 0.0.0.0 and port is 8080

Future Enhancements
1.	Resolving CSV formatting issues with data retrieved from Salesforce.
2.	Externalizing all the environment specific properties to server along with other JVM properties (wrapper.conf).
3.	Performance improvements using VM endpoints and Collection Splitter and Aggregator. (Custom Java Transformer)
4.	Batch data load for large amounts of data from Salesforce


