---
slide_id: "week-02-lecture-01-slide-024"
source_id: "week-02-lecture-01"
page: 24
week: 2
status: unseen
concepts: []
---

# Slide 24

![Original slide 24](../../../public/generated/week-02-lecture-01/slide-024.png)

## Explanation

Standard UDP sockets are connectionless. The client does not perform a TCP-style handshake; it sends an independent datagram to a destination address. A datagram is a self-contained message, but UDP does not guarantee its arrival, timing, or content [week-02-lecture-01, p. 24].

## Walkthrough

Unlike a TCP server, a UDP server does not call `listen()` or `accept()`. It binds a local port and waits for datagrams. One socket can receive from many clients and send replies to many clients because each arriving datagram carries the sender's address.

This changes the programming model:

```text
TCP: socket → bind → listen → accept → read/write
UDP: socket → bind → receive a datagram with its sender address
```

UDP preserves datagram boundaries: one received datagram corresponds to one sent unit, subject to the buffer size and the protocol's maximum message limits. It does not provide TCP's built-in ordering, retransmission, or connection state.

## Connections and exam relevance

This contrasts directly with the TCP lifecycle studied in Slides 3–23 and revisits why `SOCK_DGRAM` maps to UDP. An assessment may ask which server calls disappear, how the server knows where to reply, or what reliability guarantees are absent [week-02-lecture-01, p. 24].

## Check your understanding

Why does a UDP server not need `listen()` or `accept()`, and how does it know where to send a reply?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 24]
