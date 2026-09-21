---
slide_id: "week-02-lecture-02-slide-033"
source_id: "week-02-lecture-02"
page: 33
week: 2
status: understood
concepts: [transport-segmentation-reassembly, sequence-ordering, source-destination-transport]
---

# Slide 33

![Original slide 33](../../../public/generated/week-02-lecture-02/slide-033.png)

## Explanation

The transport layer segments application data at the source and provides a mechanism at the destination to reverse that process. Host A divides its data into several transport units, and Host B receives those units and reconstructs the original data for the application. [week-02-lecture-02, p. 33]

## Walkthrough

At Host A, the application supplies one data block to the transport layer. The transport layer adds a header to each smaller segment and passes them to the network layer. At Host B, the transport layer receives the segments from the network layer, uses the transport information to associate them with the right connection and order them, then delivers the reconstructed data upward. [week-02-lecture-02, p. 33]

## Connections and exam relevance

This is end-to-end transport segmentation, not router fragmentation. Intermediate routers forward the resulting packets; they do not normally rebuild the original application data. TCP uses sequence information and acknowledgements to support ordered, reliable reconstruction. UDP preserves datagram boundaries but does not provide TCP's full reliable reassembly service. [week-02-lecture-02, p. 33]

## Check your understanding

What does Host B’s transport layer do with the multiple segments it receives before delivering data to the application?

Student response: It collects, orders, and reconstructs the segments before delivering the data upward to the application.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 33]
