RSocket is a binary protocol for use on byte stream transports such as TCP, WebSockets, and Aeron.

support for interaction models beyond request/response such as streaming responses and push

application-level flow control semantics (async pull/push of bounded batch sizes) across network boundaries

binary, multiplexed use of a single connection

support resumption of long-lived subscriptions across transport connections

need of an application protocol in order to use transport protocols such as WebSockets and Aeron


This “RSocket” protocol is a formal communication protocol that embraces the “reactive” principles.

RSocket seeks to:
Reduce perceived latency and increase system efficiency by supporting non-blocking, duplex, async application communication with flow control over multiple transports from any language
.
Reduce hardware footprint (and thus cost and operational complexity) by:
increasing CPU and memory efficiency through use of binary encoding
avoiding redundant work by allowing persistent connections

Reduce perceived user latency by:
avoiding handshakes and the associated round-trip network overhead
reducing computation time by using binary encoding
allocating less memory and reducing garbage collection cost


Interaction Models


Request/Response (single-response)


Request/Stream (multi-response, finite)


Fire-and-Forget


Channel

References
https://rsocket.io/





