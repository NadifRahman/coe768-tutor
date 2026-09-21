---
slide_id: "week-02-lecture-01-slide-012"
source_id: "week-02-lecture-01"
page: 12
week: 2
status: unseen
concepts: []
---

# Slide 12

![Original slide 12](../../../public/generated/week-02-lecture-01/slide-012.png)

## Explanation

This slide combines the socket calls into one TCP timeline. The application first creates and prepares sockets, then the client calls `connect()` while the server calls `accept()`. TCP performs the three-way handshake underneath. Only after the connection is established does the client use `write()` and the server use `read()` to exchange application data [week-02-lecture-01, p. 12].

## Walkthrough

Read the diagram from top to bottom:

1. Client: `socket()`; server: `socket()`, `bind()`, `listen()`, and `accept()`.
2. Client: `connect()`. The TCP layer exchanges handshake packets; the calls return when the connection is established.
3. Client: `write(sd, buf, n)` sends application bytes.
4. Server: `read(sd, buf, BUFSIZ)` copies received bytes into its buffer and returns the number of bytes received.
5. TCP sends acknowledgements underneath the application calls.

The arrows labelled “return from connect” and “return from accept” emphasize that those calls are operating-system interfaces whose completion reflects TCP connection establishment. The application does not manually construct the handshake packets.

## Connections and exam relevance

This is the complete client/server trace for the concepts in Slides 3–11. An assessment may ask you to place calls in order, identify where the handshake occurs, or map a `write()` on one side to a `read()` on the other [week-02-lecture-01, p. 12].

## Check your understanding

Which events happen before the client’s `write()` call, and which component—not the application—sends the TCP acknowledgement?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 12]
