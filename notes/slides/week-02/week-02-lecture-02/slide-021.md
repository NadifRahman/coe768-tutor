---
slide_id: "week-02-lecture-02-slide-021"
source_id: "week-02-lecture-02"
page: 21
week: 2
status: understood
concepts: [physical-signal-transmission, bit-stream, media-independence]
---

# Slide 21

![Original slide 21](../../../public/generated/week-02-lecture-02/slide-021.png)

## Explanation

Physical-layer devices carry the bit stream between data-link layers. They convert bits into the appropriate physical signals and carry those signals across the medium, then recover the bit stream at the other side. Examples include hubs, NICs, and cables such as Ethernet copper or fiber optic cables. [week-02-lecture-02, p. 21]

## Walkthrough

The diagram shows a sequence such as `100101...` entering the physical layer, being represented as a signal on the medium, and emerging as the corresponding bit stream at the receiving physical layer. The data-link layers above do not need to know whether the signal travelled through copper, fiber, or another physical medium; they operate on the recovered bits and frames. [week-02-lecture-02, p. 21]

## Connections and exam relevance

This is another example of abstraction. The physical layer handles the conversion between bits and signals, while the data-link layer handles local frames. A hub or cable does not inspect IP addresses or transport ports; it simply carries or repeats the physical signal. [week-02-lecture-02, p. 21]

## Check your understanding

What does the physical layer carry across the medium, and what information does it avoid interpreting?

Student response: It carries the signal representation of the bits and does not interpret higher-level information such as IP addresses, ports, or application data.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 21]
