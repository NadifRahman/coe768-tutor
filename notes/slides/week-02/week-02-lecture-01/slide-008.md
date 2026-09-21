---
slide_id: "week-02-lecture-01-slide-008"
source_id: "week-02-lecture-01"
page: 8
week: 2
status: unseen
concepts: []
---

# Slide 8

![Original slide 8](../../../public/generated/week-02-lecture-01/slide-008.png)

## Explanation

`connect()` is the TCP client-side call that requests a connection to a server. It uses the destination IP address and port stored in `serv_addr`; if the TCP handshake succeeds, the call returns `0`, otherwise it returns `-1` [week-02-lecture-01, p. 8].

## Walkthrough

```c
int connect(int sockfd, struct sockaddr *serv_addr, int addrlen);
```

- `sockfd`: the client's socket descriptor.
- `serv_addr`: a structure containing the server's destination IP address and port.
- `addrlen`: the size of that structure.

For a TCP socket, `connect()` causes the client TCP layer to begin the three-way handshake. On success, the same client descriptor can be used with `read()` and `write()` for the established byte stream. The server counterpart is waiting on its listening socket and eventually calls `accept()` to receive a connected descriptor.

## Connections and exam relevance

This is the client-side counterpart to the server's `bind()` → `listen()` → `accept()` sequence. Be able to distinguish the destination address passed to `connect()` from the local address the client may receive automatically [week-02-lecture-01, p. 8].

## Check your understanding

After a successful TCP `connect()`, what kind of operations can the client perform using the same socket descriptor?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 8]
