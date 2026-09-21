---
slide_id: "week-02-lecture-01-slide-016"
source_id: "week-02-lecture-01"
page: 16
week: 2
status: unseen
concepts: []
---

# Slide 16

![Original slide 16](../../../public/generated/week-02-lecture-01/slide-016.png)

## Explanation

This slide begins a concrete `echo_server.c` implementation. It creates an IPv4 TCP stream socket, prepares a local server address, and binds the socket before listening [week-02-lecture-01, p. 16].

## Walkthrough

The code follows the lifecycle we have learned:

- `socket(AF_INET, SOCK_STREAM, 0)` requests an IPv4 TCP socket and stores its descriptor in `sd`.
- The `if` statement checks for `-1`; on failure it prints an error to `stderr` and exits.
- `server.sin_family = AF_INET` records the IPv4 address family.
- `server.sin_port = 3000` chooses the server's port in this example.
- `server.sin_addr.s_addr = htonl(INADDR_ANY)` asks the server to accept traffic arriving through any local interface, converting the value to network byte order.
- `bind()` associates `sd` with the address structure. The code checks its return value and exits if the address cannot be bound.
- The final comment indicates that the next step will queue up to five connection requests with `listen()`.

This is a server setup phase: no client has been accepted yet, and no application data is being exchanged.

## Connections and exam relevance

This code combines `socket()`, `bind()`, `INADDR_ANY`, error checking, and the upcoming backlog configuration. An assessment may ask you to trace which calls run before the server can accept a client or explain why each return value is checked [week-02-lecture-01, p. 16].

## Check your understanding

Before any client can connect, what address and port does this code attempt to associate with `sd`?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 16]
