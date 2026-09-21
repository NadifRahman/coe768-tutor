---
slide_id: "week-02-lecture-02-slide-024"
source_id: "week-02-lecture-02"
page: 24
week: 2
status: understood
concepts: [mac-table, switch-forwarding, frame-locality]
---

# Slide 24

![Original slide 24](../../../public/generated/week-02-lecture-02/slide-024.png)

## Explanation

This example shows a switch forwarding a frame from end system M1 to end system M2. The switch consults its MAC table, which maps MAC addresses to switch ports. Because M1 is on port 1 and M2 is on port 4, the switch forwards the frame toward port 4. [week-02-lecture-02, p. 24]

## Walkthrough

The frame carries a data-link header containing the destination MAC M2 and source MAC M1, along with the network-layer PDU/data. The switch examines the destination MAC and selects the corresponding output port. It does not need to inspect the application message or TCP/UDP contents to perform this Layer 2 decision. [week-02-lecture-02, p. 24]

## Connections and exam relevance

This is the difference between switching and routing: switching uses a MAC-to-port table for local delivery, while routing uses IP information to choose a path between networks. The frame remains within the local link/network; a router would terminate that local frame and create a new one if the packet needed to cross an IP-network boundary. [week-02-lecture-02, p. 24]

## Check your understanding

According to the table, which switch port should receive a frame whose destination MAC address is M2?

Student response: Port 4.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 24]
