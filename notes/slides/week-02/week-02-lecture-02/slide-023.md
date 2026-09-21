---
slide_id: "week-02-lecture-02-slide-023"
source_id: "week-02-lecture-02"
page: 23
week: 2
status: understood
concepts: [switching, local-area-delivery, full-duplex]
---

# Slide 23

![Original slide 23](../../../public/generated/week-02-lecture-02/slide-023.png)

## Explanation

The data-link layer handles local delivery of frames between nodes on the same local-area network. A switch is a Layer 2 device: it examines MAC addresses and sends frames through the selected destination port rather than routing based on IP addresses. [week-02-lecture-02, p. 23]

## Walkthrough

In the diagram, Source A sends a frame into the switch. The switch identifies the destination MAC address for B and forwards the frame through B's port. The other connected devices do not need to receive that unicast frame. The slide also describes the switch connection as full duplex, meaning transmission can occur in both directions at the same time. [week-02-lecture-02, p. 23]

## Connections and exam relevance

This reinforces the scope boundary: a switch forwards frames within the local network, while a router is needed when traffic must cross into another IP network. Full duplex is a property of the communication link, not a guarantee that the application sends data continuously in both directions. [week-02-lecture-02, p. 23]

## Check your understanding

If a switch receives a unicast frame addressed to Host B, what information does it use to decide which port should receive the frame?

Student response: It uses the destination MAC address to select the port.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 23]
