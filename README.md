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
