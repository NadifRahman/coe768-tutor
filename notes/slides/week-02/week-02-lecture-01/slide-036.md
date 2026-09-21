---
slide_id: "week-02-lecture-01-slide-036"
source_id: "week-02-lecture-01"
page: 36
week: 2
status: unseen
concepts: []
---

# Slide 36

![Original slide 36](../../../public/generated/week-02-lecture-01/slide-036.png)

## Explanation

This completes the UDP time-server loop: bind the socket, receive a client datagram, obtain the current time, format it as text, and send it back to the client address stored by recvfrom() [week-02-lecture-01, p. 36].

## Walkthrough

The loop works as follows:

1. bind() associates s with the server's IP address and port.
2. recvfrom() waits for a datagram and fills fsin with the client's address.
3. time(&now) obtains the current time value.
4. ctime(&now) produces a printable string, stored through pts.
5. sendto() sends that string to fsin, the client that made the request.

There is an important inconsistency in the slide: it shows listen(s, 5) after bind(), but this is a UDP server. UDP does not use listen() or accept(); the server should proceed directly to recvfrom(). The surrounding slides explicitly establish this UDP rule, so treat listen(s, 5) here as an erroneous leftover from the TCP server pattern, not as a required UDP step.

## Connections and exam relevance

This is a code-tracing exercise combining bind(), recvfrom(), time conversion, and sendto(). It also tests whether you can recognize a protocol mismatch in the sample: TCP lifecycle calls should not be copied into a standard UDP server [week-02-lecture-01, p. 36; week-02-lecture-01, p. 24].

## Check your understanding

After recvfrom() returns, which variable tells the server where to send the time reply, and should listen() be part of this UDP server?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 36]
