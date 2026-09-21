---
slide_id: "week-02-lecture-02-slide-008"
source_id: "week-02-lecture-02"
page: 8
week: 2
status: understood
concepts: [tcp-ip-reference-model, osi-to-tcp-ip-mapping, practical-layering]
---

# Slide 8

![Original slide 8](../../../public/generated/week-02-lecture-02/slide-008.png)

## Explanation

The Internet reference model, commonly called the TCP/IP model, is the practical model most associated with the Internet. Unlike the seven-layer OSI model, the diagram groups the functions into four layers: Application, Transport, Internet, and Link. [week-02-lecture-02, p. 8]

## Walkthrough

The mapping is:

- OSI Application + Presentation + Session → TCP/IP Application
- OSI Transport → TCP/IP Transport
- OSI Network → TCP/IP Internet
- OSI Data Link + Physical → TCP/IP Link

The two models organize many of the same networking responsibilities, but they use different boundaries. For example, HTTP, data representation, and session-related functions are grouped together in the TCP/IP application layer. [week-02-lecture-02, p. 8]

## Connections and exam relevance

This explains why the earlier slide called OSI a conceptual reference model while identifying TCP/IP as the model used in practice, particularly on the Internet. Do not treat the names as interchangeable: “OSI layer 3” is the network layer, while “TCP/IP Internet layer” is the corresponding practical grouping. [week-02-lecture-02, p. 8]

## Check your understanding

Which three OSI layers are combined into the TCP/IP Application layer, and which two OSI layers are combined into the TCP/IP Link layer?

Student response: OSI Application, Presentation, and Session combine into TCP/IP Application; OSI Data Link and Physical combine into TCP/IP Link.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 8]
