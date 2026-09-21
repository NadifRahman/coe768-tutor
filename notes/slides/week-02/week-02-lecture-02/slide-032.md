---
slide_id: "week-02-lecture-02-slide-032"
source_id: "week-02-lecture-02"
page: 32
week: 2
status: understood
concepts: [packet-size-limit, serialization-delay, retransmission-cost, mtu]
---

# Slide 32

![Original slide 32](../../../public/generated/week-02-lecture-02/slide-032.png)

## Explanation

Frames and packets have size limits because very large units can increase delay and make errors more expensive. A network may also require segmentation or fragmentation when the data unit is larger than the supported MTU. [week-02-lecture-02, p. 32]

## Walkthrough

On a slow link, a large frame occupies the link for longer, delaying subsequent frames. If one bit is corrupted, the entire frame or packet may need retransmission. Smaller units reduce the amount of data that must wait behind one transmission and reduce the amount that must be resent after an error.

The practical trigger shown on the slide is an MTU mismatch: if the packet or frame is larger than the network's maximum supported size, it must be segmented or fragmented. [week-02-lecture-02, p. 32]

## Connections and exam relevance

This connects the size limit to both performance and reliability. Smaller units are easier to schedule and retransmit, while the MTU ensures that a unit can physically fit into the next network's frame or packet format. The trade-off is that more units can create more per-unit header overhead. [week-02-lecture-02, p. 32]

## Check your understanding

Why can a very large packet increase both network delay and the cost of recovering from a single-bit error?

Student response: Large units occupy links longer and require more data to be retransmitted when an error occurs.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 32]
