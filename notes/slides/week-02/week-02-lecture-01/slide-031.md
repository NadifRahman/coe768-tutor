---
slide_id: "week-02-lecture-01-slide-031"
source_id: "week-02-lecture-01"
page: 31
week: 2
status: unseen
concepts: []
---

# Slide 31

![Original slide 31](../../../public/generated/week-02-lecture-01/slide-031.png)

## Explanation

UDP can be used in either unconnected or connected mode. “Connected UDP” is an application/socket configuration, not a TCP-style transport connection: calling connect() records a default remote IP address and port, but it does not perform a three-way handshake or make UDP reliable [week-02-lecture-01, p. 31].

## Walkthrough

In unconnected mode, each send specifies its destination with sendto(), and each receive can report the sender with recvfrom(). The same socket can contact different servers.

In connected UDP mode, the client calls connect() once to select one remote endpoint. It can then use send() or write() and receive with recv() or read(), much like a TCP client’s API. The underlying packets are still independent UDP datagrams; there is still no handshake, ordering guarantee, retransmission, or reliable delivery. The main benefit is convenience and a fixed peer, not TCP-like reliability.

## Connections and exam relevance

This explains the apparent tension between “UDP is connectionless” and a UDP socket using connect(). The transport remains connectionless; connect() only stores a default endpoint for the local socket [week-02-lecture-01, p. 31].

## Check your understanding

Does calling connect() on a UDP socket create a TCP-style reliable connection? What does it actually configure?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 31]
