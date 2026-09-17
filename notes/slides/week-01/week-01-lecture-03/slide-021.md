---
slide_id: "week-01-lecture-03-slide-021"
source_id: "week-01-lecture-03"
page: 21
week: 1
status: teaching
concepts:
  - adjacent-and-peer-layer-interaction
---

# Slide 21

![Original slide 21](../../../public/generated/week-01-lecture-03/slide-021.png)

## Explanation

HTTP and TCP interact in two different ways. Adjacent-layer interaction occurs within one machine: TCP provides a reliable service to the HTTP layer above it. Same-layer, or peer, interaction describes corresponding protocols on different machines, such as HTTP on the browser communicating with HTTP on the server.

## Walkthrough

There are two views:

1. **Adjacent layers:** HTTP calls TCP on the same host; TCP performs lower-level work for HTTP.
2. **Peer layers:** browser HTTP and server HTTP follow the HTTP protocol, while browser TCP and server TCP follow the TCP protocol.

The peer-layer lines are conceptual or dotted because the corresponding layers are on different machines. The actual data travels down the sender's stack, across the network, and up the receiver's stack.

## Connections and exam relevance

This distinction is important: higher layers rely on lower layers locally, while same-layer protocols define the communication rules between endpoints.

## Check your understanding

What is the difference between adjacent-layer interaction and same-layer interaction?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 21]
