---
slide_id: "week-02-lecture-02-slide-028"
source_id: "week-02-lecture-02"
page: 28
week: 2
status: understood
concepts: [router-frame-replacement, same-ip-packet, mac-hop-addressing]
---

# Slide 28

![Original slide 28](../../../public/generated/week-02-lecture-02/slide-028.png)

## Explanation

This slide gives a concrete example of frame replacement at a router. Host 1 has MAC M1 and IP P1; Host 3 has MAC M3 and IP P3. The router has MAC M4 on its first interface and M5 on its second interface. [week-02-lecture-02, p. 28]

## Walkthrough

On the first local network, Host 1 sends:

**Ethernet Frame 1: M1 → M4 | IP packet: P1 → P3 | FCS**

The switches forward this frame without becoming an end-to-end endpoint. At the router, Frame 1 is removed. The router keeps the IP packet and creates:

**Ethernet Frame 2: M5 → M3 | IP packet: P1 → P3 | FCS**

The IP source and destination remain P1 and P3, while the MAC addresses change to match the next local link. The FCS is frame-level checking information. [week-02-lecture-02, p. 28]

## Connections and exam relevance

This is the clearest example of the two addressing scopes: IP addresses represent the end-to-end route, and MAC addresses represent the current hop. The router uses its M4 interface on the first network and its M5 interface on the second network. [week-02-lecture-02, p. 28]

Clarification beyond the slide: the router does not derive a MAC address mathematically from an IP address. It first uses its routing table to choose an outgoing interface and next-hop IP address. For IPv4, ARP resolves that directly connected next-hop IP to a MAC address; for IPv6, Neighbor Discovery performs the analogous resolution. The router then builds the new local frame using the resolved next-hop MAC. If the destination is on another network, the router resolves the next router's interface MAC—not the final host's MAC. Switches simply forward the resulting frame according to its destination MAC. [week-02-lecture-02, p. 28]

## Check your understanding

After the router forwards the packet, what stays the same and what changes between Ethernet Frame 1 and Ethernet Frame 2?

Clarification question: Before sending Frame 1, how does Host 1 learn the MAC address of its default gateway, and how does the router learn the MAC address needed on its outgoing link?

Student response: Routing chooses the next hop, and ARP/NDP resolves that next-hop IP to a MAC; switches then forward the frame.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 28]
