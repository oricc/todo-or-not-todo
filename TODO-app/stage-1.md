# Stage 1 - Serve me a task

The first stage of this exercise concerns building the bare bones of the server-client architecture. In this stage, you will write a server with a database backend, as well as a client that will interact with the server.

## The Task (no pun intended)

You will create an app for managing tasks.
Each task will have the following fields:

1. Id
2. Title
3. Body
4. Due date
5. Is the task complete

## Server

The server will be written using the following technologies:

1. ASP.NET Core Web API
2. MySQL for a database

The server will have the following endpoints:

1. Add new task
2. Delete task
3. Mark task as completed
4. Delete all completed tasks


## Client

The client will be written as a Python console-line app and will provide a user-friendly interface to manage all the functionality in the server