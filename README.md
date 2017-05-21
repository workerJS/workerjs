# workerjs

WorkerJS is microservicing framework.

Main goal of this project is to provide scalable environment for running your asynchronous tasks with ability of active monitoring and problem detection. 

Philosophy behind it is to provide plug and play environment with ability of extending it to fit your own needs. You do not need to get your hands dirty but, you can. 

It consists of multiple parts. 

 * Client, library for pushing tasks and communicating with worker processes...

 * Worker, CLI application and library for starting instances of your application (processes) and forwarding tasks and providing layer for communication with client. 

 * Monitor is independent service for monitoring whole system and detecting problems, logging and making it easier for you to manage your system. 

