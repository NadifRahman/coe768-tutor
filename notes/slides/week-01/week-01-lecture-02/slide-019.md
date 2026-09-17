---
slide_id: "week-01-lecture-02-slide-019"
source_id: "week-01-lecture-02"
page: 19
week: 1
status: teaching
concepts: []
---

# Slide 19

![Original slide 19](../../../public/generated/week-01-lecture-02/slide-019.png)

## Explanation

This slide shows three ways ICMP can report the status of an IP packet: successful delivery, TTL expiration, and an unreachable destination.

## Walkthrough

**Normal case:** the destination IP matches the destination host. The host receives the packet and can send an ICMP Echo Reply back to the source.

**TTL expires:** a router decreases TTL as it forwards the packet. If the value becomes zero, the router discards the packet and sends an ICMP Time Exceeded message back to the source. The message identifies the original destination IP so the source knows which attempted delivery failed.

**Destination unreachable:** if a router cannot reach the destination network or host, it sends an ICMP Destination Unreachable message back to the source. This can happen when there is no route or the destination is unavailable.

The key relationship is: the destination IP identifies which delivery attempt the diagnostic message refers to, while TTL controls whether the packet may continue being forwarded.

Clarification: routing protocols are designed to choose loop-free paths, but temporary routing loops can occur after failures or during route convergence. TTL is the safety mechanism that guarantees a looping packet will eventually be discarded. For example, if Router A sends a packet to Router B, B mistakenly sends it back to A, and the packet starts with TTL 3, the sequence is A (2), B (1), A (0); the next router discards it and returns ICMP Time Exceeded.

The destination IP normally stays unchanged in the original packet—for example, 10.1.1.1 at the source, every router, and the destination. An ICMP error sent back to the source includes the original packet’s identifying header information, including that destination IP, so the source can tell which intended delivery the error concerns. In a real implementation, the ICMP message also includes additional identifying information from the original packet, and a ping request can be matched using its identifier and sequence number; the destination IP alone is not a globally unique packet ID.

## Connections and exam relevance

This expands the ping and TTL behavior from Slide 18 and explains how traceroute can learn about intermediate hops by provoking and observing TTL-exceeded responses. [week-01-lecture-02, p. 19]

## Check your understanding

**Check:** What is the difference between an ICMP Echo Reply, an ICMP Time Exceeded message, and an ICMP Destination Unreachable message?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 19]
