# Stage 2 - Yes Boss!

In this stage we will move the project up a notch by introducing _push notifications_.

## Part 1: Who's the boss?

Your app has really taken off!
As it is so popular, it is neccery to implement a premission model to allow users and teams to have private tasks.

In order to do so, each task will now have a user associated with it, and only that user will be able to access\modify their tasks.

Furthermore, there will be a special type of user called a **manger**.

In addition to all the user functionalities, the manager can also _subscribe_ to users (more on that in part 2).


### Functions to implement
- Add the option to login and register a new user
- Each request (except the login) will now contain an identification header to authenticate the user
- When a manager views tasks, he will see all the tasks of the users he is subscribed to as well



## Part 2: Big Brother

Managers can now recieve notification on each action a user they are subscribed to make.

This will be implemented by using RabbitMQ, a message queuing technology.

- All actions by users will be written to a exchange
- When a manager logs in, the server will bind a queue to the exchange
- The manager will subscribe to the queue and show only the messages of those users he is subscribed to
