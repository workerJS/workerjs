# Client protocol

## 1: Initialization

 * Client connects to Redis

## Task creation

 * You create task

 * Client pushes task to the top of queue

 * Client notifies monitor (if monitor is available)

 * Client subscribes to channel for that that task

 * Client gets notified after task gets assigned

## Task finish

 * Client unsubscribes form messaging channel

 * Client confirms successful or unsuccessful finish to monitor (if monitor is available)

