=========================
Microservice architecture
=========================

We apply a microservice architecture, which means that we run every service as an isolated process.

The first reason is that failure of one process should not impact another.
If, for example, the process of PDF storage fails for some reason and requires a restart, this shouldn’t impact user registration, or the registration / verification of incoming PDF’s received from suppliers.

The second reason is that microservices allow us to dynamically distribute and scale the processes independently.
One process may be more cpu intensive than another, and one process may require more time to process compared to another.
Depending on the cluster technology used, we will be able to choose for an optimal setup in which we can monitor and scale different processes dynamically depending on the need that we observe.

In order to save on initial cost, it should be sufficient to use a single database.
