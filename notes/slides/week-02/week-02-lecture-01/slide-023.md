---
slide_id: "week-02-lecture-01-slide-023"
source_id: "week-02-lecture-01"
page: 23
week: 2
status: unseen
concepts: []
---

# Slide 23

![Original slide 23](../../../public/generated/week-02-lecture-01/slide-023.png)

## Explanation

This slide shows the echo application logic on both sides. The server reads bytes from the connected client socket and writes the same bytes back. The client reads input from the keyboard, sends it to the server, reads the echoed response, and writes that response to standard output [week-02-lecture-01, p. 23].

## Walkthrough

### Server: `echod(int sd)`

```c
while (n = read(sd, buf, BUFLEN)) {
    write(sd, buf, n);
}
close(sd);
```

The server repeatedly receives chunks from the client and sends each chunk back. When `read()` returns `0`, the client has ended its stream, so the server closes the connected descriptor.

### Client

The client reads keyboard input from descriptor `0`, sends it with `write(sd, sbuf, n)`, and then reads the response from the socket. Because a TCP `read()` may return fewer bytes than the echoed message, the client tracks `bytes_to_read` and advances the buffer pointer `bp` until the expected number of bytes has arrived. It prints the received message to descriptor `1`, standard output.

The slide annotates Ctrl-D as end-of-file on the keyboard input; when the input read returns `0`, the client closes its socket.

## Connections and exam relevance

This combines `read()`, `write()`, `close()`, TCP stream framing, and standard Unix descriptors. A code-tracing question could ask which direction each `read()` or `write()` moves data, or why the client performs a loop while receiving the echo [week-02-lecture-01, p. 23].

## Check your understanding

Why does the client need a receiving loop after it sends a message, instead of assuming one `read()` returns the complete echoed message?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 23]
