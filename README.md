# nervosum
A distributed system nervous system.

```
consistency : weak (try once), strong(ack-loops through in-memory, local persist or remote through replication)
receivers : pid0, ..., pidN

http://node/send/
{
 receivers,
 consistency,
 message
}

http://node/recv/MessageType
```

### Goals

 - Protocol driven distributed overlay network
 - Simple APIs
 - Test driven
 - Metrics driven
 - Launch through dynamic topologies
 - Interfaces are _only_ HTTP

### Terminology

```
Protocol:

MessageGroup {
  NodeClass => NodeClass : MessageType
}
```
