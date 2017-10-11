# Why not HTTP? 

A lot of people use HTTP for communication. 

So, why did we decide not to use HTTP? 

## How is HTTP connection established? 

HTTP uses TCP and with it inherits slow socket opening (up to multiple RTT). 

![img](https://static.lwn.net/images/2012/tfo/3whs.png)

## TCP VS UDP

Since we are not going to use HTTP, we are back to choosing protocol. 

We can use either some kind of hybrid or we have TCP vs UDP situation. 

### Why is TCP still an option? 

Problem with HTTP is that for each request we need to open socket. 
We can use protocol that keeps socket open (even multiple sockets for parallelism).

### So, what about UDP? 

Problem with UDP is that package loss is possible and this could end up in system failure. 

### Maybe hybrid? 

At this stage of project, it is too complicated to implement custom protocol on top of UDP with data integrity check, so, at this moment, this is not an option. 

## Initial decision? 

We will use TCP with sockets opened in advance and waiting. 