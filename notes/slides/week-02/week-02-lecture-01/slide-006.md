---
slide_id: "week-02-lecture-01-slide-006"
source_id: "week-02-lecture-01"
page: 6
week: 2
status: unseen
concepts: []
---

# Slide 6

![Original slide 6](../../../public/generated/week-02-lecture-01/slide-006.png)

## Explanation

`bind()` assigns a socket to a local network address: an IP address plus a transport-layer port. Servers use it to claim the address where clients should reach them [week-02-lecture-01, p. 6].

## Walkthrough

```c
int bind(int sockfd, struct sockaddr *my_addr, int addrlen);
```

- `sockfd`: the descriptor returned by `socket()`.
- `my_addr`: a pointer to a `sockaddr` structure containing the local IP address and port.
- `addrlen`: the size of that structure, typically `sizeof(struct sockaddr)`.

The return value is `0` for success and `-1` for failure. A port value of `0` asks the operating system to choose an available ephemeral port. `INADDR_ANY` means the server should accept traffic addressed to any of the machine's local interfaces rather than naming one specific local IP address.

## Connections and exam relevance

`bind()` follows `socket()` and precedes `listen()` on a TCP server. It is also used with UDP, because UDP needs a local port to receive datagrams. An assessment may test which address is local, why a server usually uses a known port, or what special values `0` and `INADDR_ANY` mean [week-02-lecture-01, p. 6].

## Check your understanding

Why does a server normally bind to a known port, while a client can often let the operating system choose its local port?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 6]
