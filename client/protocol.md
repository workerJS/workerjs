# Client protocol

## 1) Initialization

 * Client connects to Redis

## 2) Task creation

 * You create task

 * Client subscribes to channel for that that task

 * Client pushes task to the top of queue

 * Client notifies monitor (if monitor is available)

 * Client gets notified after task gets assigned (in channel)

 * **Client gets notified on retry/failure**

## 3) Task finish/failure

 * Client unsubscribes form messaging channel

 * Client ACKs finish to monitor

