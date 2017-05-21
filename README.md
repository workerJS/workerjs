# workerjs

WorkerJS is microservicing framework.

Main goal of this project is to provide scalable enviroment for running your asynchronus tasks with ability of active monitoring and problem detection. 

Philosophy behind it is to provide plug and play enviroment with ability of extending it to fit your own needs. You do not need to get your hands dirty but, you can. 

It consists of multiple parts. 

 * Client, library for pushing tasks and communicating with worker processess...

 * Worker is CLI application for starting instances of your application (processess) and forwarding tasks and providing layer for cummunication with client. 

 * Monitor is independant service for monitoring whole system and detecting problems, logging and making it easier for you to manage your system. 

