---
slide_id: "week-02-lecture-01-slide-009"
source_id: "week-02-lecture-01"
page: 9
week: 2
status: unseen
concepts: []
---

# Slide 9

![Original slide 9](../../../public/generated/week-02-lecture-01/slide-009.png)

## Explanation

`accept()` completes the server side of a pending TCP connection. It removes one connection request from the listening socket's queue and returns a new descriptor for communication with that client. The original server socket remains a listening socket and can accept more clients [week-02-lecture-01, p. 9].

## Walkthrough

```c
int accept(int sockfd, struct sockaddr *cliaddr, socklen_t *addrlen);
```

- `sockfd`: the listening socket descriptor.
- `cliaddr`: storage for the connecting client's IP address and port.
- `addrlen`: the size of that address structure; it is passed by pointer because the system may update it.

On success, the return value is a non-negative connected-socket descriptor. On failure, it returns `-1`. The usual server pattern is to keep `sockfd` for listening and use the returned descriptor for `read()` and `write()` with one client.

## Connections and exam relevance

This completes the server side of the TCP setup: `listen()` manages a queue, and `accept()` turns one queued request into an application-visible connection. The key exam distinction is that one listening descriptor can produce many connected descriptors [week-02-lecture-01, p. 9].

## Check your understanding

After `accept()` returns a new descriptor, which descriptor should the server use for client data, and which descriptor should it keep for future clients?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 9]
