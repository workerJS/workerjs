# Multiplexer external protocol

## 1) Initialization

 * Multiplexer connects to Redis

 * Multiplexer starts listening in the queue

## 2) Task recieved

 * Multiplexer subscribes to channel for that task

 * Multiplexer notifies monitor about taking task (if monitor is available)

 * Multiplexer notifies client about taking task

## 3) Retry (in case of failure/timeout, when TTL > 0 and retry enabled)

 * Multiplexer notifies monitor about task retry (if monitor is available)

 * Multiplexer notifies client about task retry

## 4) Task finish/failure

 * Multiplexer notifies monitor

 * Multiplexer notifies client

 * Multiplexer unsibscribes from channel

## 5) Multiplexer shuting down or crash

 * Multiplexer retries all tasks (if they are eliable)

 * Multiplexer unsubscribes form queue

