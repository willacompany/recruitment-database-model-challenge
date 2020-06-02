# Database Model Population Challenge

Home assignment for candidates.

## Background

At Willa we use the principle of [Infrastructure as code](https://en.wikipedia.org/wiki/Infrastructure_as_code) to setup and manage our technology stack. This makes continuous integration and deployment easy, does minimize error-prone manual processes, as well as makes sure developers also own the implications of how their solutions are put into production.

Here our (fictional) database model is defined as JSON file, containing an array of table definitions. A table column may be a foreign key, matching a column in another table.

When automatically creating tables, they must be created in an order to ensure no table is created with a foreign key, before the referenced table itself is created.

I.e. table `users` with column `id` must be created before table `invoices` with column `created_by_user` that has foreign key defined as `users.id`.

## Challenge

Your challenge is to write a program that reads the data from `database.json` and outputs table names sorted in an order that allow the tables to be created. Assume your program will be used with any other data conforming to the same specification.

Preferably use **TypeScript** or **JavaScript** in your solution.

Submit the your source code, with tests to prove the result, to a Github repository and share it with your technical contact person at Willa.

Good luck! 👋
