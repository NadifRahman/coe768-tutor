---
slide_id: "week-02-lecture-02-slide-014"
source_id: "week-02-lecture-02"
page: 14
week: 2
status: understood
concepts: [frame-reencapsulation, ip-packet-across-links, layered-forwarding]
---

# Slide 14

![Original slide 14](../../../public/generated/week-02-lecture-02/slide-014.png)

## Explanation

This slide shows the same end-to-end message travelling through different link technologies. The hosts use HTTP, TCP, and IP above the local link. The router removes the incoming Ethernet frame and re-encapsulates the IP packet inside a SONET frame for the next link, then the packet is placed inside another Ethernet frame near the destination. [week-02-lecture-02, p. 14]

## Walkthrough

At the sending host, the data is wrapped as:

**Message → TCP segment → IP packet → Ethernet frame**

At the router, the Ethernet wrapper is removed. The router forwards the IP packet across the middle network as:

**SONET frame → IP packet → TCP segment → message**

On the final link, it becomes an Ethernet frame again. The message, TCP information, and IP packet conceptually continue end-to-end, while the link-layer frame changes for each local network. [week-02-lecture-02, p. 14]

Clarification: SONET is typically a link technology used in an intermediate carrier or core network. The source host may send an Ethernet frame to its first router, whose outgoing interface places the IP packet into a SONET frame. A router at the far edge of that SONET network removes the SONET framing and places the same IP packet into an Ethernet frame for the destination's local network. In the reverse direction, the process happens in reverse: Ethernet enters the edge router, SONET carries the packet through the core, and Ethernet is used again near the source. [week-02-lecture-02, p. 14]

## Connections and exam relevance

This is re-encapsulation at the link layer. It demonstrates why HTTP does not need to know whether the network uses Ethernet or SONET: HTTP data is carried by TCP, TCP is carried by IP, and IP can be placed inside whatever link-layer frame the next hop requires. [week-02-lecture-02, p. 14]

## Check your understanding

When the packet enters the SONET portion of the path, which part is replaced: the HTTP message, the TCP segment, the IP packet, or the link-layer frame?

Clarification question: Which devices are likely to perform the Ethernet-to-SONET and SONET-to-Ethernet transitions—the end hosts or routers at the edges of the intermediate network?

Student response: The edge routers perform the link-layer transition while forwarding the IP packet through the intermediate network.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 14]
