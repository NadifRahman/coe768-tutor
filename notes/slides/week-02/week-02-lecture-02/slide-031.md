---
slide_id: "week-02-lecture-02-slide-031"
source_id: "week-02-lecture-02"
page: 31
week: 2
status: understood
concepts: [transport-segmentation, ip-fragmentation, mtu]
---

# Slide 31

![Original slide 31](../../../public/generated/week-02-lecture-02/slide-031.png)

## Explanation

Segmentation and fragmentation divide large data units into smaller units so they can fit the limits of the network path. Transport-layer segmentation divides application data into transport segments. IP-layer fragmentation divides an IP packet/datagram when a link has a smaller Maximum Transmission Unit (MTU). [week-02-lecture-02, p. 31]

## Walkthrough

The MTU is the largest packet or frame size, in bytes, that a particular network can carry. In the example, Ethernet supports an MTU of 1500 bytes, but the intermediate Frame Relay network supports only 512 bytes. A packet that fits on Ethernet may therefore need to be fragmented before crossing the smaller-MTU network. The fragments travel onward and are reassembled at the destination. [week-02-lecture-02, p. 31]

## Connections and exam relevance

Keep the terminology separate: transport segmentation produces multiple transport-layer segments from application data, while IP fragmentation splits an IP packet/datagram to fit a lower-layer MTU. The purpose is to adapt data units to transmission-size limits without changing the overall communication endpoints. [week-02-lecture-02, p. 31]

Clarification: MTU is more like a maximum vehicle/package size than the number of lanes. A smaller-MTU network cannot carry one oversized packet, so the packet may be split into smaller IP fragments. In the slide's IPv4 example, the destination reassembles the fragments; intermediate routers normally forward the fragments rather than reassembling them. Transport segments, by contrast, are reassembled by the destination transport layer. [week-02-lecture-02, p. 31]

## Check your understanding

Why might a router need to fragment an IP packet when forwarding it from a network with a 1500-byte MTU into a network with a 512-byte MTU?

Clarification question: In the slide's IPv4 example, which endpoint reassembles the IP fragments—the intermediate router or the destination host?

Student clarification: IP packets/fragments are carried inside local data-link frames. Frames are hop-by-hop and may be replaced at routers, while IP fragments remain part of the end-to-end network-layer transfer until the destination reassembles them.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 31]
