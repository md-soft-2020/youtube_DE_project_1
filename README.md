# Convert an existing Relational data model into a Dimensional data model

A data warehouse is almost exclusively built in a form of a dimensional data model (or Star schema). The goal here is to :
>- facilitate readibility of the database by non-technical people.
>- facilate queries performance with less joins to be performed between tables.

Dataset here: https://www.postgresqltutorial.com/postgresql-getting-started/postgresql-sample-database/

Note: Initial DB is a relational database respecting the Normalisation (3NF) rules. This DB contains the following tables:
>- Actor
>- addrerss
>- category
>- city
>- country
>- customer
>- film
>- film_actor
>- film_category
>- inventory
>- language
>- payment
>- rental
>- staff
>- store


# Leanings from this project

STEP 1: Understand the Business & Ops Process → Data from the Business point of View

>- What are definitions of variables ? What does each variable mean ?
>- How are data related to each other ?
>- How do the end-users expect to use the data for ? e.g: dashboard for metrics
>- etc.

STEP 2: Understand the source of the data

>- Where is the data coming from ?
>- What are specificities about the data: 
>>- Real-time/non real-time data coming in in the DB.(< 5 mn)
>>- Huge/low volume of data coming in the DB ?  
>>- etc.

N.B: The understanding of the data source will allow you to choose the type of database (Relational DB, Graph DB, etc).

STEP 3: Building a Data warehouse

>- From an existing (relational) database model (or relational data model), we can build a dimensional data model (or Star schema). To do so, find tables that can be combined/aggregated into one to avoid duplication.
>- We build a data warehouse to have good queries permanence:
>>- No need to do many JOINs to get specific data, as we would do in a relational DB.
>>- Less JOINs means then lower query execution time
