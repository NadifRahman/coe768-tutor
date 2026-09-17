---
slide_id: "week-01-lecture-03-slide-009"
source_id: "week-01-lecture-03"
page: 9
week: 1
status: teaching
concepts: []
---

# Slide 9

![Original slide 9](../../../public/generated/week-01-lecture-03/slide-009.png)

## Explanation

TCP establishes a connection before the applications exchange data, synchronizing the two endpoints and allowing the server to accept or refuse the connection.

## Walkthrough

The connection begins with the **three-way handshake**:

1. The client sends `SYN`, requesting a connection.
2. The server replies `SYN/ACK`, accepting and acknowledging the request.
3. The client sends `ACK`, confirming that it received the server’s response.

Once the connection is established, the applications exchange data, and TCP acknowledgements confirm receipt. When communication is finished, the endpoints exchange `FIN` and `ACK` messages to close the connection cleanly.

Clarification: TCP is full duplex, so both endpoints can send data independently. A TCP connection has two directions, and each side can begin closing its own direction with `FIN`; the other side acknowledges it and may close its direction separately. The diagram’s request/reply appearance does not mean TCP is limited to request–response. HTTP or REST commonly uses request–response at the application layer, while WebSockets also use TCP underneath but maintain a persistent bidirectional application exchange after setup.

## Connections and exam relevance

This explains what the earlier slide meant by TCP’s reliable, connection-oriented service. The socket API exposes operations such as connect, accept, send, and receive, while TCP performs the handshake, acknowledgements, and orderly close underneath. [week-01-lecture-03, p. 9]

## Check your understanding

**Check:** What is the purpose of TCP’s three-way handshake before application data is sent?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 9]
