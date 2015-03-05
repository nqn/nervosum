# nervosum
A distributed system nervous system.

```
consistency : weak (try once), strong(ack-loops through in-memory, local persist or remote through replication)
receivers : pid0, ..., pidN

send(receivers, consistency, message)
recv<MessageType>()
```

### Goals

 - Protocol driven distributed overlay network
 - Simple APIs
 - Test driven
 - Metrics driven

### Terminology

```
Protocol:

MessageGroup {
  NodeClass => NodeClass : MessageType
}
```
