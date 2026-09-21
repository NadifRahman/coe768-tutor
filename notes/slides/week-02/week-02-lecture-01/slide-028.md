---
slide_id: "week-02-lecture-01-slide-028"
source_id: "week-02-lecture-01"
page: 28
week: 2
status: unseen
concepts: []
---

# Slide 28

![Original slide 28](../../../public/generated/week-02-lecture-01/slide-028.png)

## Explanation

Closing a TCP socket terminates that endpoint's participation in a connection, potentially in one direction at a time. UDP has no standard connection state to terminate, but its socket still consumes a kernel file descriptor and other resources, so the program should call close() when finished [week-02-lecture-01, p. 28].

## Walkthrough

The important distinction is between **connection termination** and **resource cleanup**:

- TCP close() participates in ending an established byte-stream connection.
- UDP close() does not end a handshake-established connection, because standard UDP has no such connection; it releases the socket descriptor and associated kernel resources.

The same general rule applies to sockets as to files: once the program no longer needs the descriptor, close it. A long-running UDP server usually keeps its bound socket open while serving, then closes it during shutdown.

## Connections and exam relevance

This reinforces the TCP/UDP distinction and the fact that a socket is an operating-system resource even when the protocol is connectionless. An assessment may ask whether UDP needs close() and why the answer is still yes [week-02-lecture-01, p. 28].

## Check your understanding

If UDP has no connection to terminate, why should a UDP program still call close()?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 28]
