---
slide_id: "week-02-lecture-05-slide-003"
source_id: "week-02-lecture-05"
page: 3
week: 2
status: understood
concepts: [frame-check-sequence, fcs, crc, encapsulation, trailer]
---

# Slide 3

![Original slide 3](../../../public/generated/week-02-lecture-05/slide-003.png)

## Explanation

The data-link layer detects frame corruption using a **Frame Check Sequence (FCS)**. The FCS is an error-detection value calculated from the frame contents, commonly using a **Cyclic Redundancy Check (CRC)** algorithm. [week-02-lecture-05, p. 3]

## Walkthrough

The left side shows encapsulation through the layers: application data is passed downward, and each layer may add control information. At the data-link layer, a header is placed before the data and the FCS is placed after it as a **trailer**:

`[link header | upper-layer data | FCS]`

The physical layer then transmits the frame as a sequence of signals. At the receiving end, the link layer calculates or verifies the FCS over the received frame. If the value does not match, the frame is considered corrupted. The FCS covers the link-layer frame, including the upper-layer data carried inside it; it does not mean that the link layer understands the application’s content. [week-02-lecture-05, p. 3]

## Connections and exam relevance

This is why error detection appears at multiple layers: each layer can protect the data it receives. A link-layer FCS catches corruption on the local link, while transport or application mechanisms may provide additional end-to-end checks. FCS detection normally identifies corruption; it does not by itself repair the frame. [week-02-lecture-05, p. 3]

## Check your understanding

What is the purpose of the FCS, and where is it placed in the data-link frame?

Student response: The FCS detects corruption and is placed in the frame trailer.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-05, p. 3]
