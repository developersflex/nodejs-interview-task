# Flex Business Solutions Tech Test - BookStore

In Flex Business Solutions, we aim to provide excellence and efficiency on all our lines of code in order to support the day-to-day activities of the company using our software solutions. In doing so, we use microservices to seperate the concerns of the codebase. Microservices help us when we need to make a change to functionality — and deploy that functionality in a way that the rest of the system doesn't have to change. 

In this task, we would like you to build a simple BookStore API. It should provide a `user` service and an accompanying `book` service to work with. In this case the user service backs a front end admin tool allowing non-technical staff to interact with data. A request has been submitted by the stakeholders for a new admin feature:

## Requirements

- A user is able to generate a csv formatted report showing the values of all user book readings
    - The report should be sent to the `/export` route of the users service
    - The users service expects the report to be sent as csv text
    - The csv should contain a row for each user matching the following headers
    |User Id|First Name|Last Name|Date|Book|Pages Read|
    - The Book should be the name of the book given by the books service
    - The Pages Read can be calculated by `totalPages * percentageRead`
- Ensure use of up to date packages and libraries
- Make effective use of git

We prefer:
- Functional code
- Unit testing

### Notes
All of you work should take place inside the `admin` microservice

We're interested in how you break down the work and build your solution in a clean, reusable and testable manner. You can use any packages that would help with this task.

## Deliverables
**Please make sure to update the readme with**:

- Your new routes
- How to run any additional scripts or tests you may have added
- Relating to the task please add answers to the following questions;
    1. How might you make this service more secure?
    2. How would you make this solution scale to millions of records?
  

On completion email a link to your repository to your contact at Flex Business Solutions and ensure it is publicly accessible.

## Getting Started

Please clone this repository and push it to your own github (or other) public repository
To develop you will need to start each service seperately with

```bash
npm start
or
npm run develop
```

The develop command will run nodemon allowing you to make changes without restarting (they use ports 8081, 8082 and 8083)
Use Postman or any API tool of you choice to trigger your endpoints (this is how we will test your new route).

### Existing routes
We have provided a series of routes 

Users - localhost:8081
- `/users` get all users
- `/users/:id` get a user record by id
- `/users/export` expects a csv formatted text input as the body

Books - localhost:8082
- `/books` get all book details
- `/books/:id` get book by id

Admin - localhost:8083
- `/users/:id` get a user record by id
