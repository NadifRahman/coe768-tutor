---
slide_id: "week-02-lecture-01-slide-026"
source_id: "week-02-lecture-01"
page: 26
week: 2
status: unseen
concepts: []
---

# Slide 26

![Original slide 26](../../../public/generated/week-02-lecture-01/slide-026.png)

## Explanation

sendto() sends one datagram through a UDP socket to a destination address. Unlike TCP write(), it supplies the destination as part of the call [week-02-lecture-01, p. 26].

## Walkthrough

    int sendto(int sockfd, const void *msg, int len,
               unsigned int flags, const struct sockaddr *to,
               int tolen);

- sockfd: UDP socket descriptor.
- msg: buffer containing the datagram payload.
- len: payload length in bytes.
- flags: normally 0 in this course.
- to: destination IP address and port.
- tolen: size of the destination address structure.

The return value is the number of bytes sent, or -1 on error. Conceptually, the call packages the payload as one datagram and asks UDP/IP to deliver it to the specified endpoint. The destination can change from one call to the next, which is why one UDP socket can communicate with multiple peers.

## Connections and exam relevance

This is the UDP counterpart to TCP write(). The key difference is that sendto() includes an explicit destination and preserves the datagram as one message unit. An assessment may ask you to identify which structure contains the destination or interpret the return value [week-02-lecture-01, p. 26].

## Check your understanding

What information does sendto() use to decide where the UDP datagram should go, and how is this different from TCP write()?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 26]
