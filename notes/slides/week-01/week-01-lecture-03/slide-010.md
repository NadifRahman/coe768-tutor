---
slide_id: "week-01-lecture-03-slide-010"
source_id: "week-01-lecture-03"
page: 10
week: 1
status: teaching
concepts: []
---

# Slide 10

![Original slide 10](../../../public/generated/week-01-lecture-03/slide-010.png)

## Explanation

TCP termination uses a four-message exchange because the two directions of a full-duplex connection close independently.

## Walkthrough

The usual sequence is:

1. One endpoint sends `FIN`, indicating it will send no more data in its direction.
2. The other endpoint sends `ACK`.
3. After finishing any remaining data in the opposite direction, it sends its own `FIN`.
4. The first endpoint sends the final `ACK`.

This allows one side to stop sending while still receiving remaining data from the other side. Once both directions are closed, the connection’s buffers and port-related resources can be released. Either client or server can initiate the process.

## Connections and exam relevance

This explains the FIN/ACK sequence previewed on Slide 9 and reinforces TCP’s full-duplex behavior: connection setup synchronizes both endpoints, while termination closes each direction safely. [week-01-lecture-03, p. 10]

## Check your understanding

**Check:** Why are two FIN messages needed instead of one to terminate a TCP connection?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 10]
