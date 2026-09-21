---
slide_id: "week-02-lecture-02-slide-010"
source_id: "week-02-lecture-02"
page: 10
week: 2
status: understood
concepts: [protocol-data-unit, encapsulation, pdu-names]
---

# Slide 10

![Original slide 10](../../../public/generated/week-02-lecture-02/slide-010.png)

## Explanation

PDU means **Protocol Data Unit**: the complete unit handled at a particular layer. A PDU generally contains the data from the higher layer plus control information such as a header and sometimes a trailer. Each layer gives the resulting unit a different name. [week-02-lecture-02, p. 10]

## Walkthrough

The names used in the TCP/IP stack are:

- Application → message or data
- Transport → segment
- Network → packet
- Data link → frame
- Physical → bit

As data moves downward, each layer can add its own header or trailer around the existing data. This is encapsulation. At the physical layer, there is no protocol header in the same sense—the information is represented as a sequence of physical signals/bits. [week-02-lecture-02, p. 10]

## Connections and exam relevance

This gives precise vocabulary for packet diagrams and exam questions. Strictly speaking, TCP produces a segment, while UDP commonly produces a datagram; the slide uses “segment” as the general transport-layer PDU name. The key idea is that the same application data is wrapped with different control information as it passes through the stack. [week-02-lecture-02, p. 10]

## Check your understanding

Why does a physical-layer transmission not have a normal header, while a transport-layer PDU can have one?

Student response: The physical layer transmits raw bits as signals, while higher layers need metadata and control flags to interpret and manage the data.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 10]
