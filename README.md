# salesforceconnectorapi

SALESFORCE CONNECTOR API - MULESOFT

        1.  I created a RAML specification using the Anypoint Studio to design the REST APIs and then created Mule Flows using the RAML Specification.
        2.  All the configurations are externalized using properties files (mule-app.properties, http.properties, salesforce.properties)
        3.	Global Configurations are a part of globalconfigurations.xml, which can be reused across various Mule flows in the application.
        4.	Dataweave is used to transform the data retrieved from Salesforce into CSV
        5.	A file component creates a file using the inputs from the Dataweave

GETTING STARTED

        1.	Import the project into MuleSoft Anypoint Studio
        2.	Change the salesforce.properties to use valid salesforce login credentials
        3	Change the FILE_PATH in mule-app.properties

PREREQUISITES

        1.	Mulesoft Anypoint Studio EE (I used 6.4.2)
        2.	Java (I used Java 8)

RUNNING

        1.	There are two main APIs as described below that retrieve Account details from Salesforce using the MuleSoft Salesforce Connector
        2.	API can be accessed at http://<hostName>:<port>/salesforce/getAllAccounts and 
        3.	http://<hostName>:<port>/salesforce/getAccountByName?name=xyz
        4.	Default Values for host 0.0.0.0 and port is 8080

FUTURE WORK

        1.	Resolving CSV formatting issues with data retrieved from Salesforce.
        2.	Externalizing all the environment specific properties to server along with other JVM properties (wrapper.conf).
        3.	Performance improvements using VM endpoints and Collection Splitter and Aggregator. (Custom Java Transformer)
        4.	Batch data load for large amounts of data from Salesforce
