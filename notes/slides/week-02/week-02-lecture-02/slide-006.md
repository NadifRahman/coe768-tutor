---
slide_id: "week-02-lecture-02-slide-006"
source_id: "week-02-lecture-02"
page: 6
week: 2
status: understood
concepts: [transport-layer-functions, network-layer-routing, logical-addressing]
---

# Slide 6

![Original slide 6](../../../public/generated/week-02-lecture-02/slide-006.png)

## Explanation

This slide introduces two lower layers. The transport layer is responsible for moving application messages between hosts and can provide connection control, flow control, and error control. The network layer delivers packets from source to destination across multiple interconnected networks using logical addressing and routing. [week-02-lecture-02, p. 6]

## Walkthrough

At the transport layer, connection control distinguishes connectionless communication from connection-oriented communication. Flow control prevents a fast sender from overwhelming a slow receiver. Error control detects problems in messages, using error-detection codes.

At the network layer, a logical address identifies where a device is located in the network, and routing determines which path packets should take toward their destination. A useful distinction is that transport concerns the end-to-end delivery service, while network routing concerns getting packets across a collection of networks. [week-02-lecture-02, p. 6]

## Connections and exam relevance

This connects to the earlier TCP/IP discussion: TCP provides transport-layer connection, flow, and reliability mechanisms, while IP provides network-layer addressing and routing. UDP is also a transport-layer protocol, but it is connectionless and provides fewer delivery guarantees than TCP. [week-02-lecture-02, p. 6]

## Check your understanding

Which layer decides the route a packet takes across multiple networks, and which layer manages issues such as a fast sender overwhelming a slow receiver?

Student answer: The network layer decides how a packet moves through multiple networks, and the transport layer manages a slow receiver through flow control.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 6]
