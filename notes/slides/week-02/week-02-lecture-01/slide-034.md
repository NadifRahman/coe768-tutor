---
slide_id: "week-02-lecture-01-slide-034"
source_id: "week-02-lecture-01"
page: 34
week: 2
status: unseen
concepts: []
---

# Slide 34

![Original slide 34](../../../public/generated/week-02-lecture-01/slide-034.png)

## Explanation

This introduces a UDP time server. It waits for a client datagram requesting the server's current time, then sends the time back. It is iterative because one request is received and answered at a time [week-02-lecture-01, p. 34].

## Walkthrough

The variables prepare the server logic:

- fsin stores a client's socket address.
- buf[100] is a temporary input/output buffer.
- pts will point to a formatted time string.
- sock is the server's UDP socket descriptor.
- now stores the current time value.
- alen stores the length of the client address structure for recvfrom().

The next slides fill in the socket creation, binding, receive, time conversion, and reply steps. The key application protocol is request/reply: the client's datagram is the request, and the returned time string is the response.

## Connections and exam relevance

This applies the UDP datagram pattern to a useful service and reinforces that the server needs the client's address in order to reply. An assessment may ask you to identify which variables hold the socket, payload, timestamp, and peer address [week-02-lecture-01, p. 34].

## Check your understanding

Why must the time server keep the client's address in fsin?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 34]
