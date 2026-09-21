---
slide_id: "week-02-lecture-01-slide-027"
source_id: "week-02-lecture-01"
page: 27
week: 2
status: unseen
concepts: []
---

# Slide 27

![Original slide 27](../../../public/generated/week-02-lecture-01/slide-027.png)

## Explanation

recvfrom() receives one UDP datagram and records the sender's address. It returns the number of payload bytes copied into the buffer, or -1 on error [week-02-lecture-01, p. 27].

## Walkthrough

    int recvfrom(int sockfd, void *buf, int len,
                 unsigned int flags, struct sockaddr *from,
                 int *fromlen);

- sockfd: UDP socket descriptor.
- buf: destination buffer.
- len: maximum buffer capacity.
- flags: normally 0.
- from: storage for the sender's IP address and port.
- fromlen: size of the address structure, supplied by pointer.

Unlike TCP read(), recvfrom() returns one datagram at a time and tells the server who sent it. The server can then pass the recorded address to sendto(). The buffer must be large enough for the datagram the application expects; UDP does not turn one datagram into a stream of smaller reads.

## Connections and exam relevance

This is the receiving counterpart to sendto() and completes the UDP request/reply pattern. An assessment may ask which parameter receives the peer address or contrast one-datagram-at-a-time behavior with TCP's stream-oriented read() [week-02-lecture-01, p. 27].

## Check your understanding

What extra information does recvfrom() provide that an ordinary buffer read does not?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 27]
