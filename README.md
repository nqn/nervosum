# nervosum
A distributed system nervous system.

```
consistency : weak (try once), strong(ack-loops through in-memory, local persist or remote through replication)
receivers : pid0, ..., pidN

send(receivers, consistency, message)
```
