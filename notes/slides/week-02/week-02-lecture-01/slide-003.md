---
slide_id: "week-02-lecture-01-slide-003"
source_id: "week-02-lecture-01"
page: 3
week: 2
status: unseen
concepts: []
---

# Slide 3

![Original slide 3](../../../public/generated/week-02-lecture-01/slide-003.png)

## Explanation

This slide maps the TCP client/server conversation to socket API calls. A **socket** is the program's handle to a network communication endpoint. The client actively connects; the server prepares a listening endpoint and waits for clients. Once a connection is accepted, both sides use read/write operations to exchange a request and reply [week-02-lecture-01, p. 3].

## Walkthrough

On the server side:

- `socket()` creates a socket.
- `bind()` associates it with a local address and port.
- `listen()` marks it as ready to receive connection requests.
- `accept()` blocks—waits—until a client completes connection establishment. It then provides a connected socket for this particular client.
- `read()` receives the request; the server processes it and uses `write()` to send the reply.
- Another `read()` can observe the end-of-file/close notification, after which the server calls `close()`.

On the client side:

- `socket()` creates its endpoint.
- `connect()` triggers the TCP three-way handshake.
- `write()` sends the request.
- `read()` receives the reply.
- `close()` ends the connection.

The subtle but important server distinction is that the listening socket is used to wait for clients, while `accept()` yields a separate connected socket used for the actual data exchange.

## Connections and exam relevance

This is the concrete implementation of the handshake and request–reply sequence from Slides 1–2. A likely assessment skill is tracing the correct call order and identifying which calls block or create a communication endpoint [week-02-lecture-01, p. 3].

## Check your understanding

Why does the server need both `listen()` and `accept()`? Also, which side calls `connect()`?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 3]
