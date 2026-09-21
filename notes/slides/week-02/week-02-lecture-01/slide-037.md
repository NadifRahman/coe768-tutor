---
slide_id: "week-02-lecture-01-slide-037"
source_id: "week-02-lecture-01"
page: 37
week: 2
status: unseen
concepts: []
---

# Slide 37

![Original slide 37](../../../public/generated/week-02-lecture-01/slide-037.png)

## Explanation

This final slide shows a connected-UDP client for the time service. It creates a UDP socket, associates it with the server address using connect(), sends a request with write(), reads the time reply, prints it, and exits [week-02-lecture-01, p. 37].

## Walkthrough

The client flow is:

    s = socket(AF_INET, SOCK_DGRAM, 0);
    connect(s, &sin, sizeof(sin));
    write(s, MSG, strlen(MSG));
    n = read(s, (char *)&now, sizeof(now));
    write(1, now, n);

The call to connect() records the server's IP address and port locally; it does not perform a TCP handshake. The write() sends a UDP datagram to that selected server, and read() receives a datagram from the selected peer. Descriptor 1 is standard output, so the final write displays the response.

This completes the Week 2 progression from socket creation and addressing through TCP server concurrency and UDP request/reply programming.

## Connections and exam relevance

This example combines connected UDP, network byte order/address structures, read/write, and the request/reply pattern. An assessment may ask you to compare this client with the unconnected UDP client using sendto()/recvfrom(), or explain why connect() does not make UDP reliable [week-02-lecture-01, p. 37].

## Check your understanding

What does connect() configure in this UDP client, and why is it still accurate to call the underlying protocol connectionless?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 37]
