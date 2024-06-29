## Every bit of content writter in this .md file was extracted by IBM course as BackEnd Developer and serves the only purpose of knowledge through this module

This content was extracted from coursera's IMB Django course
What is data? 

As you start this course, you will be introduced to concepts fundamental to understanding data, databases, and database management systems. You will learn some basic SQL statements. Explore the structure, use cases, and limitations of relational databases. Learn key relational database concepts, including entities, attributes, entity-relationship data modeling, common data types, and primary key. You will learn about cloud database fundamentals and get hands-on experience creating a database instance on the cloud. At the end of the module, an optional lesson with more advanced SQL techniques will help you get the most out of your data.

Learning Objectives
1. Write basic SQL statements
2. Describe relational databases
3. Discuss the use cases and limitations of relational databases.
4. Define data and databases
5. Describe relational database concepts such as entities, attributes, entity-relationship models, and primary key
6. Define non-relational databases and their characteristics.
7. Create a database instance on the Cloud
8. Provide the syntax and examples for the following SQL statements: SELECT, INSERT, UPDATE, and DELETE

______________________________________________________________________________________________________
Relational Database:

A relational DB is a collection of data organized into a table structure, where the tables can be linked, or related, based on data common to each.

Enables to retrieve data in one or more tables based on relationship between structured tables. 

1. Ideal for optimized storage, retrieval, processing of data for large volumes of data
2. Each table has a unique set of rows and columns
3. Relationships da be restricted to specific data types and values
4. Can retrieve millions of records in seconds using SQL for querying data
5. Security architecture of relational dbs provides greater access control and governance

Advantages of relational dbs are:

- Create meaningful information by joining tables.
- Flexibility to make changes while the database is in use
- Minimize data redundancy
- Offer export and import option that proved ease of backup and disaster recovery
- Are ACID Compliant (Atomicity consistency, isolation and durability.) 

Use Cases:
1. Online Transaction Processing (OLTP) application
2. Data Warehouses
3. IoT Solutions 

Limitations:
1. Does not work well with semi-structured and unstructured data
2. Migration between rdbms is possible only when they've identical schemas and data types
3. Entering a value greater than the defined lenght of a data field results in loss of information

______________________________________________________________________________________________________

NoSQL or Non SQL is a non-relational database design that provides flexible schemas for the storage and retrieval of data.

- Gained greater popularity due to the emergence of cloud computing, big data, and high-volume web and mobile applications
- Chosen for their attributes around scale, performance, and ease of use
- Built for specific data models
- Flexible schemas that allow programmers to create and manage modern applications
- Do not use a traditional row/column/table database design with fixed schemas
- Do not, tipically, use the structured query language (or SQL) to query data

Common types of NoSQL:
1. Key-value database (Redis, Memcached, DynamoDB) :
    - Data in a key-value db is store as pairs
    - A key represents an attribute of the data and is a unique identifier.
    - Both keys and values can be anything from integers to JSON complex document.


2. Document-Based (mongoDB) database :
    - Document databases store each record and its associated data within a single document
    - They Enable flexible indexing, powerful and hoc queries, and analytics over collections of documents.
    - Preferred for eCommerce platforms, medical recordsm CRM platforms and analytics platforms.

3. Column-Based (Apache HBASE):
    - Data is stored in cells grouped as columns of data instead of rows
    - All cells corrisponding to a column are saved as a continuous disk entry, making access and search easier and faster.
    - Great for systems that require heavy write requests, storing time-series data, weather data, and IoT data.

4. Graph-Based (CosmosDB):
    - Use graphical model to represent and store data
    - Useful for visualizing, analyzing, and finding connections between different pieces of data.
    - Excellent choice for connected data
    - Great for Social networks, Product recommendations, Network diagrams, Fraud detection, Access management

Advantages of NoSQL:

1. Its ability to handle large volumes of structured, semi-structured, and unstructured data
2. Its ability to run as a distributed system scaled across multiple data centers
3. An efficient and cost-effective scale-out architecture that provides additional capacity and performance with the addition of new nodes 
4. Simpler design, better control over availability, and improved scalability that makes it agile, flexible and support quick iterations