---
slide_id: "week-02-lecture-01-slide-032"
source_id: "week-02-lecture-01"
page: 32
week: 2
status: unseen
concepts: []
---

# Slide 32

![Original slide 32](../../../public/generated/week-02-lecture-01/slide-032.png)

## Explanation

This slide emphasizes that connected UDP is mainly a convenience for a client that communicates with one server. The application specifies the server once, then can send multiple datagrams without repeating the destination address [week-02-lecture-01, p. 32].

## Walkthrough

Calling connect() on UDP records the server's IP address and port in the local socket. It does not send a TCP-style handshake and does not change UDP into a connection-oriented or reliable protocol. The datagrams remain independent, and UDP still provides no built-in retransmission or ordering.

The practical API effect is convenience: after the remote endpoint is selected, the client can use send()/write() and recv()/read() rather than supplying an address on every send and receiving one on every receive. This mode is appropriate when the client has one intended server at a time; unconnected mode is more flexible when destinations vary.

## Connections and exam relevance

This is a reinforcement slide for the distinction between a socket API configuration and a transport protocol property. An assessment may present connect() on a UDP socket and ask whether a handshake or reliability has been introduced [week-02-lecture-01, p. 32].

## Check your understanding

What practical convenience does connected UDP provide, and what important TCP properties does it still lack?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 32]
