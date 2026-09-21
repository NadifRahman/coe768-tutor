---
slide_id: "week-02-lecture-02-slide-007"
source_id: "week-02-lecture-02"
page: 7
week: 2
status: understood
concepts: [data-link-layer, physical-layer, local-delivery, signal-representation]
---

# Slide 7

![Original slide 7](../../../public/generated/week-02-lecture-02/slide-007.png)

## Explanation

The data link layer transfers data between two devices on the same local network. It is similar to the network layer in that it can provide flow control and error control, but its scope is local rather than source-to-destination across multiple networks. The physical layer sends bits as signals and defines how those bits are represented electrically, optically, or through radio waves. [week-02-lecture-02, p. 7]

## Walkthrough

Imagine a packet travelling from a laptop to a router on the same Wi-Fi or Ethernet network. The data link layer manages that one-hop transfer. The physical layer converts the bits into signals—such as voltage changes on a cable, light pulses in fiber, or radio waves over Wi-Fi. At the next router, the packet may be placed into a new link-layer frame for the next local hop. [week-02-lecture-02, p. 7]

## Connections and exam relevance

Keep the scopes separate: the network layer chooses a multi-network route, the data link layer handles delivery over one local link, and the physical layer handles the actual signal representation. The slide notes that the OSI model remains useful for describing network architecture even though the complete seven-layer arrangement is complex and is not always implemented as distinct practical layers. [week-02-lecture-02, p. 7]

## Check your understanding

What is the difference between the data link layer and the physical layer when sending a frame over Wi-Fi or Ethernet?

Student response: The data link layer manages local delivery and related control, while the physical layer represents and transmits the bits as electrical, optical, or radio signals.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 7]
