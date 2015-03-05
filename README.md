# Nervosum

A distributed system nervous system.

## Goals

- Protocol driven distributed overlay network
- Simple APIs
- Test driven
- Metrics driven
- Launch through dynamic topologies
- Interfaces are _only_ HTTP

## Dimensions of point-to-point messaging

**Delivery Guarantee**

- At most once
  - Retry
  - Backoff
  - TTL
- At least once
- Exactly once

**Ordering**

- Messages be delivered in send-order (per sender)
- Messages delivered in any order

**Receivers**

- Set of endpoints
- Broadcast

## Terminology

**Protocol**

```
MessageGroup {
  NodeClass => NodeClass : MessageType
}
```

## API Sketches

```http
POST /node/send HTTP/1.1
Accept: application/json
Accept-Encoding: gzip, deflate
Host: my.api.com
User-Agent: Nervosum/0.1.0

{
 receivers,
 consistency,
 message
}
```

```http
POST /node/recv HTTP/1.1
Accept: application/json
Accept-Encoding: gzip, deflate
Host: my.api.com
User-Agent: Nervosum/0.1.0

{
  uuid: XXYYZZ
}
```

```http
POST /node/ack HTTP/1.1
Accept: application/json
Accept-Encoding: gzip, deflate
Host: my.api.com
User-Agent: Nervosum/0.1.0

{
  uuid: XXYYZZ
}
```
