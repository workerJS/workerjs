# Worker external protocol

## 1) Initialization

 * Worker connects to Redis

 * Worker starts listening in the queue

## 2) Task recieved

 * Worker subscribes to channel for that task

 * Worker notifies monitor about taking task (if monitor is available)

 * Worker notifies client about taking task

## 3) Retry (in case of failure/timeout, when TTL > 0 and retry enabled)

 * Worker notifies monitor about task retry (if monitor is available)

 * Worker notifies client about task retry

## 4) Task finish/failure

 * Worker notifies monitor

 * Worker notifies client

 * Worker unsibscribes from channel

## 5) Worker shuting down or crash

 * Worker retries all tasks (if they are eliable)

 * Worker unsubscribes form queue

