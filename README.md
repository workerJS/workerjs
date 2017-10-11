# workerjs

## What is the problem we want to solve? 

When you are developing small application it is very easy to forget about future and create monolithic application. 

At the moment when you start scaling, you start facing quite complicated problems and it is very easy to take wrong turn. 

At that moment it is very important to be able to be able to split application into peaces and tackle problems independently. 

### What are benefits of splicing application into pieces? 

 * Ability develop pieces with different tools
 * Ability to run multiple instances of same application part
   * Scalability
   * Redundancy
 * Security by separating responsibility

### What are downsides of splicing application into pieces? 

* Race conditions
* Communication overhead
* Complexity for deployment

## Concept of endless problem

If you used computer in last 10 years, you know about updates and how often they happen. 

As a software developers we are aware that it is never possible to solve problem 100%. 

That is why we decided to create this open source book to help us understand problem better and choose direction for further development, together with you. 

## What is direction in which we are going at this moment? 

At this moment we are focused on developing communication platform and experimenting on which solution provides best results for our problem. 

## Client, contractor and inspection

This is the relationship that worked well for quite long time. 

Client creates contract with contractor and inspection makes sure contract is executed properly. 

### Architecture

 * Client, layer for communication with worker

 * Worker, layer for communication with your service

 * Monitor, independent service for testing system performance and health

