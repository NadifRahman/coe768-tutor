---
slide_id: "week-02-lecture-01-slide-005"
source_id: "week-02-lecture-01"
page: 5
week: 2
status: unseen
concepts: []
---

# Slide 5

![Original slide 5](../../../public/generated/week-02-lecture-01/slide-005.png)

## Explanation

`socket()` asks the operating system to create a communication endpoint and returns a **socket descriptor**—an integer handle that later calls use. If creation fails, it returns `-1` [week-02-lecture-01, p. 5].

## Walkthrough

The three arguments select the networking behavior:

- `domain`: the address family. `AF_INET` means IPv4; `AF_INET6` means IPv6.
- `type`: the communication style. `SOCK_STREAM` provides a TCP byte stream; `SOCK_DGRAM` provides UDP datagrams; `SOCK_RAW` exposes lower-level packets such as ICMP.
- `protocol`: the specific protocol. A value of `0` asks the system to choose the default protocol for the selected domain and type.

Thus `socket(AF_INET, SOCK_STREAM, 0)` means “create an IPv4 stream socket and use the default protocol,” which is TCP. The descriptor is not itself an IP address or port; it is the local program's handle for operating on the endpoint.

The names describe the abstraction seen by the application. A **stream** is one continuous, ordered flow of bytes: TCP does not preserve the boundaries between separate `write()` calls. A **datagram** is a self-contained message: each send remains a distinct unit, as with UDP. UDP does not guarantee delivery, ordering, or retransmission; the application handles any recovery it needs [week-02-lecture-01, p. 24].

`SOCK_RAW` is different because it gives the application access below TCP and UDP. ICMP is not carried by TCP or UDP; it is its own IP-layer protocol. For example, `ping` sends an ICMP Echo Request and receives an ICMP Echo Reply. The protocol is identified by the socket's `protocol` argument—commonly `IPPROTO_ICMP`—and, on a captured IPv4 packet, by the IPv4 header's Protocol field. In other words, “raw” means fewer transport-layer abstractions, not “unknown protocol.” The application or operating system must provide more of the packet-handling logic itself, and raw sockets commonly require elevated privileges [week-02-lecture-01, p. 5].

## Connections and exam relevance

This explains the parameters used in the previous slide's code and introduces the TCP/UDP distinction at the API level. An assessment may ask you to infer the protocol selected from a `socket()` call or identify the correct error result [week-02-lecture-01, p. 5].

## Check your understanding

What protocol is selected by `socket(AF_INET, SOCK_STREAM, 0)`, and why is ICMP neither TCP nor UDP when used with a raw socket?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 5]
