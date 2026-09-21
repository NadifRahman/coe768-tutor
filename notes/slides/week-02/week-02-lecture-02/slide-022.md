---
slide_id: "week-02-lecture-02-slide-022"
source_id: "week-02-lecture-02"
page: 22
week: 2
status: understood
concepts: [data-link-framing, mac-forwarding, local-flow-error-control]
---

# Slide 22

![Original slide 22](../../../public/generated/week-02-lecture-02/slide-022.png)

## Explanation

The data-link layer packages an upper-layer PDU into a frame and delivers it across one physical link. It uses MAC/Ethernet addresses to identify the local destination. Data-link devices such as switches use this information to forward frames within a local network. [week-02-lecture-02, p. 22]

## Walkthrough

The diagram shows framing: a starting delimiter (SD) marks the beginning of the frame, the PDU carries the upper-layer data, and an ending delimiter (ED) marks the boundary. This lets the receiver recognize complete data blocks rather than treating the entire bit stream as one undivided sequence.

The data-link layer can also provide error and flow control over the physical link. A switch then forwards the frame according to its destination MAC address. [week-02-lecture-02, p. 22]

## Connections and exam relevance

This connects directly to the earlier PDU vocabulary: the network-layer packet is carried inside a data-link-layer frame. The frame is local to one link; when the packet reaches a router and moves to the next link, the old frame is removed and a new frame is created. [week-02-lecture-02, p. 22]

## Check your understanding

Why does the data-link layer need framing if the physical layer already transmits a sequence of bits?

Student response: The physical layer sends a continuous stream of bits/signals, so framing provides logical boundaries for complete frames.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 22]
