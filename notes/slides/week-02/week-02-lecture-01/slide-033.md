---
slide_id: "week-02-lecture-01-slide-033"
source_id: "week-02-lecture-01"
page: 33
week: 2
status: unseen
concepts: []
---

# Slide 33

![Original slide 33](../../../public/generated/week-02-lecture-01/slide-033.png)

## Explanation

This slide shows the API simplification produced by connected UDP. The client calls connect() once, then uses write() to send datagrams to that selected server and read() to receive datagrams from it. The server remains unconnected: it uses recvfrom() and sendto() because it may receive from and reply to many clients [week-02-lecture-01, p. 33].

## Walkthrough

The client flow is:

    socket() -> connect() -> write() -> read() -> close()

The IP address and port are stored when connect() selects the remote endpoint, so write() and read() do not need the server address on every call. On the server side:

    socket() -> bind() -> recvfrom() -> sendto()

The server receives each datagram together with its sender address and uses that address for the reply. Connected UDP is therefore asymmetric in this example: only the client has selected one default peer.

Even though the calls look like TCP calls, the underlying data is still UDP datagrams, not a reliable TCP byte stream.

## Connections and exam relevance

This is the concrete API comparison between connected and unconnected UDP. An assessment may ask why the client can use read()/write() while the server still needs recvfrom()/sendto(), or whether this changes UDP reliability [week-02-lecture-01, p. 33].

## Check your understanding

After the client calls connect() on its UDP socket, why can it use write() without supplying the server’s IP address each time?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 33]
