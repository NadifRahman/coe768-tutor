---
slide_id: "week-02-lecture-01-slide-011"
source_id: "week-02-lecture-01"
page: 11
week: 2
status: unseen
concepts: []
---

# Slide 11

![Original slide 11](../../../public/generated/week-02-lecture-01/slide-011.png)

## Explanation

`close()` releases a socket descriptor and ends that endpoint's participation in the communication. It returns `0` on success and `-1` on error [week-02-lecture-01, p. 11].

## Walkthrough

```c
int close(int sockfd);
```

The argument is the descriptor to close. A client normally closes its connected socket after finishing its request and receiving the reply. A server closes the connected descriptor for one client when that session ends, but normally keeps the original listening descriptor open so it can accept future clients. At the TCP level, closing contributes to the orderly FIN/ACK termination sequence introduced earlier.

## Connections and exam relevance

This completes the basic TCP socket lifecycle: create, address, listen/connect, accept, exchange bytes, and close. An assessment may test which descriptor is closed after a client session and whether the listening socket should also be closed [week-02-lecture-01, p. 11].

## Check your understanding

When a server finishes communicating with one client, which socket should it close: the connected descriptor returned by `accept()`, the listening descriptor, or both?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 11]
