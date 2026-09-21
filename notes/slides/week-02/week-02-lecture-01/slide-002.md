---
slide_id: "week-02-lecture-01-slide-002"
source_id: "week-02-lecture-01"
page: 2
week: 2
status: unseen
concepts: []
---

# Slide 2

![Original slide 2](../../../public/generated/week-02-lecture-01/slide-002.png)

## Explanation

The slide asks how application data is transmitted reliably using TCP. The key idea is that the application does not implement reliability itself; it gives data to TCP, and TCP manages connection setup, ordered delivery, acknowledgements, retransmission when needed, and orderly shutdown. The two boxes represent TCP at the client and TCP at the server, with an application process above each TCP layer [week-02-lecture-01, p. 2].

## Walkthrough

Read the central timeline from top to bottom:

1. The client requests a connection with `SYN`.
2. TCP performs the three-way handshake: `SYN`, `SYN/ACK`, then `ACK`. This establishes shared connection state and confirms that both endpoints can communicate.
3. The server reports the connection to its application.
4. The client application gives data to its TCP layer.
5. TCP carries the data to the server.
6. The server TCP acknowledges receipt, and the server application receives the data.

At the bottom, `FIN` and `ACK` messages close the connection in an orderly way. The important distinction is that the application thinks in terms of “connect” and “send data,” while TCP performs the control-message exchange underneath.

## Connections and exam relevance

This builds directly on Week 1's client/server request–reply model and the TCP reliability concept. An assessment could ask you to trace the order of handshake messages, identify which direction an acknowledgement travels, or distinguish application data from TCP control segments [week-02-lecture-01, p. 2].

## Check your understanding

Why does the three-way handshake happen before the blue data messages? In your own words, explain what the `SYN`, `SYN/ACK`, and final `ACK` accomplish.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 2]
