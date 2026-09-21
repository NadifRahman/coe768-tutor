---
slide_id: "week-02-lecture-01-slide-013"
source_id: "week-02-lecture-01"
page: 13
week: 2
status: unseen
concepts: []
---

# Slide 13

![Original slide 13](../../../public/generated/week-02-lecture-01/slide-013.png)

## Explanation

An **iterative server** handles clients serially: it accepts one connection, completes that client’s work, closes the connected socket, and only then returns to accept another client [week-02-lecture-01, p. 13].

## Walkthrough

The cycle is:

1. Accept one incoming connection.
2. Handle the request completely.
3. Close that client’s connected descriptor.
4. Return to listening on the well-known server port.

While the server is busy with the current client, other clients cannot receive application-level service from it. Their requests may wait in the kernel’s backlog queue, but the server does not process them concurrently. A slow client can therefore delay every client behind it.

## Connections and exam relevance

This uses the listening and connected-descriptor distinction from earlier slides. An assessment may ask you to predict what happens when multiple clients arrive or identify the performance limitation of serial handling [week-02-lecture-01, p. 13].

## Check your understanding

What happens to client B if an iterative server is still processing a long request from client A?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 13]
