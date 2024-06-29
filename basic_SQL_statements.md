## Every bit of content writter in this .md file was extracted by IBM course as BackEnd Developer and serves the only purpose of knowledge through this module

<_________________________________________________________________________>

* SELECT Statement 

SELECT is a data manipulation language statement used to read and modify data through a query

Code Examples:

1. SELECT * FROM Book -> Retrieves the entire entity of Book
2. SELECT book_id, title, edition FROM Book -> Retrieves only the requested attr from entity

The order of the columns displayed always matches the order in the SELECT statement 

To restrict the result set we can use the WHERE Clause. It always requires a predicate:
- Evaluates to: True, False or Unknown
- Use in the search condition of the WHERE clause

-> SELECT Book_id, Title, ReleaseYear FROM Book WHERE Book_id='B1'
    All the comparis operator can be used

! COUNT, DISTINCT, LIMIT

COUNT -> SELECT COUNT(ReleaseYear) FROM Book WHERE ReleaseYear = '2023' -> returns the count of how many books where released in 2023

DISTINCT -> SELECT DISTINT(Title) FROM Book Where Title ='Learning Python' -> returns unique line hiding other duplicates

LIMIT -> SELECT * FROM Book LIMIT 10 -> returns only the first 10 rows of the table

<_________________________________________________________________________>

* INSERT STATEMENT 

We use the INSERT statement to populate a table with data in rows

Basic syntax is: INSERT INTO [TableName]<([ColumnName],...)> VALUES ([Value],...)

In the case of our Entity "Author", that has as attributes Author_ID, Lastname, Firstname, Email, City, Country :

INSERT INTO AUTHOR (AUTHOR_ID, LASTNAME, FIRSTNAME, EMAIL, CITY, COUNTRY) VALUES ('a1', 'Chong', 'Raul', 'rfc@imb.com', 'Toronto', 'CA')

Multiple rows can be populated simultaneously

<_________________________________________________________________________>

* UPDATE Statement

is a Data Manipulation Language statement used to alter data in a table

Basic Syntax: UPDATE[TableName] SET[[ColumnName]=[Value]] <WHERE [Condition]>

UPDATE AUTHOR SET LASTNAME='KATTA' FIRSTNAME='LAKSHMI' WHERE AUTHOR_ID='A2'


<_________________________________________________________________________>

* DELETE Statement

Basic Syntax: DELETE FROM [TableName] <WHERE [Condition]>

DELETE FROM AUTHOR WHERE AUTHOR_ID IN('A2','A3')

Negletting to use the WHERE Clause will end in deleting all rows inside the DB, so..careful!


<_________________________________________________________________________>

* CREATE statement

Syntax:

CREATE TABLE table_name
    (
        column_name_1 datatype optional_parameters,
        column_name_2 datatype,
        ...
        column_name_n datatype
    )

Taking a book's author as example, the table would be like:

CREATE TABLE author (
        author_id CHAR(2) PRIMARY KEY NOT NULL,
        lastname VARCHAR(15) NOT NULL,
        firstname VARCHAR(15) NOT NULL,
        email VARCHAR(40), 
        city VARCHAR(15),
        country CHAR(2)
    )

! NOT NULL allows for a field to not contain a null value

<LITTLE RECAP>

SELECT * FROM Entity;
INSERT INTO * FROM Entity;
UPDATE * SET[[column]=[value]] Entity;
DELETE FROM * when ****

<FINISH>

<_________________________________________________________________________>

*ALTER TABLE statement

1. Add or remove columns
2. Modify the data type of columns 
3. Add or remove keys
4. Add or remove constraints

Syntax:

ALTER TABLE table_name
    ADD COLUMN telephone_number BIGINT;
    ALTER COLUMN telephone_number SET DATA TYPE CHAR(20);
    DROP COLUMN telephone_number;


<_________________________________________________________________________>

*DROP statement

DROP TABLE table_name; (careful, it delete the entire table therefore you'll lose the data)

<_________________________________________________________________________>

*TRUNCATE statement

allows for eliminating the data in a table without touching the table itself

TRUNCATE TABLE table_name
    IMMEDIATE; 