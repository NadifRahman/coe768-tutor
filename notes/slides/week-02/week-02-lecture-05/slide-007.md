---
slide_id: "week-02-lecture-05-slide-007"
source_id: "week-02-lecture-05"
page: 7
week: 2
status: understood
concepts: [checksum-vs-crc, crc, error-detection-strength, retransmission]
---

# Slide 7

![Original slide 7](../../../public/generated/week-02-lecture-05/slide-007.png)

## Explanation

Checksums and CRCs both detect corruption, but they make different trade-offs. A checksum is generally simpler and cheaper to compute, while a CRC uses polynomial division and usually provides stronger detection for common transmission-error patterns. [week-02-lecture-05, p. 7]

## Walkthrough

The slide’s comparison is:

- **Checksum:** simpler to calculate, weaker in its detection properties, and widely used in Internet protocols such as IP, TCP, and UDP.
- **CRC:** more computationally involved, but stronger for detecting many single- and multi-bit or burst-error patterns. It is widely used at the link layer, including Ethernet, 802.11, and DSL.

If a CRC check fails, the receiver rejects the frame. The sender may retransmit when it does not receive an acknowledgement. The CRC itself detects the error; the retransmission protocol performs recovery. [week-02-lecture-05, p. 7]

## Connections and exam relevance

The choice depends on the layer’s needs. Internet protocols often favor a lightweight checksum over their own header or payload, while link technologies favor CRC because a corrupted frame should be detected before it is accepted on that local link. [week-02-lecture-05, p. 7]

## Check your understanding

Why might a link-layer protocol choose CRC even though a checksum is cheaper to compute?

Student response: CRC is more computationally involved but provides stronger error detection, especially at the link layer.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-05, p. 7]
