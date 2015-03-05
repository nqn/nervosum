# nervosum
A distributed system nervous system.

```
consistency : weak (try once), strong(ack-loops through in-memory, local persist or remote through replication), ordering (in-order, out of order)
receivers : pid0, ..., pidN

http POST http://node/send/
{
 receivers,
 consistency,
 message
}

http GET http://node/recv/MessageType
{
  uuid: XXYYZZ
}

http POST http://node/ack/
{
  uuid: XXYYZZ
}
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
