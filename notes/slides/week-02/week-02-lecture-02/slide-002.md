---
slide_id: "week-02-lecture-02-slide-002"
source_id: "week-02-lecture-02"
page: 2
week: 2
status: understood
concepts: [osi-seven-layers, logical-peer-connections, protocol-layer-mapping]
---

# Slide 2

![Original slide 2](../../../public/generated/week-02-lecture-02/slide-002.png)

## Explanation

This diagram shows the seven OSI layers on both the sending and receiving hosts. The same layer on each host is shown with a horizontal blue “logical connection”: for example, the sender's transport layer conceptually communicates with the receiver's transport layer. In the actual system, data moves down the sender's stack, crosses the network, and moves up the receiver's stack. [week-02-lecture-02, p. 2]

## Walkthrough

Read the diagram in two directions:

- Vertically inside each host, the green arrows represent interaction between neighboring layers.
- Horizontally between hosts, the blue arrows represent peer-layer communication as an abstraction.

The example maps common Internet protocols to OSI layers: HTTP is shown at the application layer, TCP at the transport layer, IP at the network layer, and Ethernet at the link layer. The physical layer carries the actual signals. A message using HTTP does not jump directly from one computer's application layer to the other; it is passed downward through the sender's layers, transmitted, then passed upward through the receiver's layers. [week-02-lecture-02, p. 2]

## Connections and exam relevance

This is the concrete version of encapsulation and decapsulation from the previous lecture. “Logical connection” does not mean a separate wire exists between every pair of corresponding layers. It means each layer is designed as though it communicates with its peer, while the real movement occurs through the stack and the underlying network. The protocol labels also connect this lecture to the earlier HTTP/TCP/IP/Ethernet stack. [week-02-lecture-02, p. 2]

## Check your understanding

If an HTTP message is sent from one host to another, does it physically travel horizontally from the sender's application layer to the receiver's application layer? Describe the actual path through the two stacks.

Student response: It travels down the sender's stack, crosses the network, and travels up the receiver's stack; the horizontal peer-layer arrows are logical connections.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 2]
