This repository contains a Python and Node.js based Voting App, designed to demonstrate the deployment and orchestration of a multi-service application using Docker Swarm.

OVERVIEW
Voting Application: Developed using Python, this app allows users to cast their votes. The application is deployed with 2 replicas to ensure load balancing and high availability.

Redis Database: Utilized Redis to manage and store voting information efficiently.

Worker Application: A .NET Worker application orchestrates the data transfer from Redis, processing the votes and storing the results in a Postgres database.

Result Display: The application retrieves the results from Postgres and displays them to the users.

Services
The application comprises the following services:

voting_app: The main voting interface where users can cast their votes.
my-redis: The Redis database for storing voting data.
worker: A .NET application that processes the votes from Redis and stores them in Postgres.
my-postgres: The Postgres database for storing the processed vote results.
result-app: The application interface for displaying the voting results.
Deployment

