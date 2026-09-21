---
slide_id: "week-02-lecture-04-slide-001"
source_id: "week-02-lecture-04"
page: 1
week: 2
status: understood
concepts: [link-layer-overview, frame-encapsulation, packet-to-frame]
---

# Slide 1

![Original slide 1](../../../public/generated/week-02-lecture-04/slide-001.png)

## Explanation

The link layer receives a network-layer packet and encapsulates it into a frame that can be sent over one local link by the physical layer. A frame typically contains a link-layer header, the network-layer packet as its payload, and a trailer. At the receiving side, the link layer processes the frame and delivers the packet upward to the network layer. [week-02-lecture-04, p. 1]

## Walkthrough

The sending path is:

`Network packet → Link header + packet + link trailer → Physical-layer transmission`

The receiver reverses this process: it recognizes the frame, checks its link-layer information, removes the header and trailer, and passes the contained packet to the network layer. The physical layer still represents the frame bits as signals; the link layer reasons about the frame structure. [week-02-lecture-04, p. 1]

## Connections and exam relevance

This continues the previous lecture's PDU hierarchy: a network packet is carried inside a link-layer frame, and the frame is carried as physical signals. The frame is local to the current link, so a router may remove one frame and create another for the next link. [week-02-lecture-04, p. 1]

## Check your understanding

What does the link layer add around a network-layer packet to turn it into a frame?

Student response: It adds a header and a trailer.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-04, p. 1]
