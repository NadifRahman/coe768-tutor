---
slide_id: "week-02-lecture-01-slide-029"
source_id: "week-02-lecture-01"
page: 29
week: 2
status: unseen
concepts: []
---

# Slide 29

![Original slide 29](../../../public/generated/week-02-lecture-01/slide-029.png)

## Explanation

This is a simple unconnected UDP echo client. It creates a datagram socket, discovers the server's address, sends one user message with sendto(), receives the server's reply with recvfrom(), and prints the reply [week-02-lecture-01, p. 29].

## Walkthrough

The code follows this sequence:

1. socket(AF_INET, SOCK_DGRAM, 0) creates an IPv4 UDP socket.
2. The omitted address-resolution code fills serveraddr and serverlen.
3. The client obtains a message in buf.
4. sendto() sends the message explicitly to serveraddr.
5. recvfrom() waits for one reply and records the sender address.
6. printf() displays the echoed text.

There is no bind(), connect(), listen(), or accept() in this basic client. The operating system can choose the client's local ephemeral port. The call shown uses the buffer's intended message length; in production code, the receive call should be given the actual capacity of the destination buffer, not a length computed from uninitialized or incoming data.

## Connections and exam relevance

This is the concrete client implementation of the UDP flow from Slides 24–27. An assessment may ask you to identify where the destination address is used, why no handshake occurs, or which call receives the reply [week-02-lecture-01, p. 29].

## Check your understanding

Which call tells the client where the server is, and which call receives the echoed datagram?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 29]
