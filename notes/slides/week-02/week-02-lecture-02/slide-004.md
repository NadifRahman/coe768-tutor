---
slide_id: "week-02-lecture-02-slide-004"
source_id: "week-02-lecture-02"
page: 4
week: 2
status: understood
concepts: [presentation-layer, data-translation, encryption-and-compression]
---

# Slide 4

![Original slide 4](../../../public/generated/week-02-lecture-02/slide-004.png)

## Explanation

The presentation layer prepares data so that different systems can interpret it consistently. Its responsibilities include formatted representations and translation services, as well as encryption and compression. The slide uses character encoding as an example: EBCDIC is associated with IBM mainframes, while ASCII is used by many other systems. [week-02-lecture-02, p. 4]

## Walkthrough

Suppose a Windows computer communicates with an IBM mainframe. The two systems may represent characters differently. The presentation layer helps translate the representation so that the receiving system interprets the transmitted data correctly. It can also transform the data by encrypting it for confidentiality or compressing it to reduce its size before lower layers transmit it. [week-02-lecture-02, p. 4]

## Connections and exam relevance

The presentation layer is about the **meaning and representation of data**, not about choosing a route or delivering bytes between endpoints. This is why it sits above the transport, network, and link responsibilities. In the OSI framework, it acts as a compatibility and data-format boundary between the application and the lower layers. [week-02-lecture-02, p. 4]

## Check your understanding

Why might two computers need a presentation-layer translation service even if the network successfully delivers every transmitted bit?

Student answer: Different systems can represent data differently, so encoding or other representation changes may be needed for both systems to interpret the data consistently. Clarification: encryption protects confidentiality, while encoding/translation addresses compatibility.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 4]
