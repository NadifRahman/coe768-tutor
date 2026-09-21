---
slide_id: "week-02-lecture-01-slide-004"
source_id: "week-02-lecture-01"
page: 4
week: 2
status: unseen
concepts: []
---

# Slide 4

![Original slide 4](../../../public/generated/week-02-lecture-01/slide-004.png)

## Explanation

This slide instantiates the previous call sequence with two IPv4 hosts. The server is at `10.1.1.1` and listens on port `10000`; the client is at `20.1.1.1` and is assigned an ephemeral port, shown as `32111`. Together, the two endpoint addresses identify the TCP connection [week-02-lecture-01, p. 4].

## Walkthrough

`socket(AF_INET, SOCK_STREAM, 0)` means:

- `AF_INET`: use IPv4 addresses.
- `SOCK_STREAM`: request a reliable byte-stream socket, implemented by TCP.
- `0`: let the system choose the appropriate protocol for that socket type.

The server binds `sd` to `10.1.1.1:10000`, listens, and calls `accept()`. The client calls `connect()` using the server's address. The server's `accept()` returns `new_sd`, the connected socket associated with this client; the original `sd` remains the listening socket.

The slide also defines a **process** as an instance of a program currently running. A server process may create child processes so multiple client connections can be handled concurrently.

## Connections and exam relevance

This connects the abstract socket workflow to addressing, ports, and file-descriptor-like socket handles. Be able to explain why the server's fixed port is advertised while the client's port may be dynamically selected, and why `new_sd` is used for communication [week-02-lecture-01, p. 4].

## Check your understanding

In this example, what is the purpose of `new_sd`, and why is it different from the server's original `sd`?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 4]
