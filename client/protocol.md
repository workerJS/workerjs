# Client protocol

## 1) Initialization

 * Client connects to Redis

## 2) Task creation

 * You create task

 * Client subscribes to channel for that that task

 * Client pushes task to the top of queue

 * Client notifies monitor (if monitor is available)

 * Client gets notified after task gets assigned

## 3) Task finish

 * Client unsubscribes form messaging channel

 * Client confirms successful or unsuccessful finish to monitor (if monitor is available)

