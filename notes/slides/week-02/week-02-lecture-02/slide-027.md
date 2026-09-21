---
slide_id: "week-02-lecture-02-slide-027"
source_id: "week-02-lecture-02"
page: 27
week: 2
status: understood
concepts: [packet-path, routing-and-switching, source-destination-forwarding]
---

# Slide 27

![Original slide 27](../../../public/generated/week-02-lecture-02/slide-027.png)

## Explanation

This diagram illustrates a packet travelling from source A to destination B through a collection of switches and a router. The red path highlights the selected route: local switches forward the frame within each local network, while the router connects the different IP networks and forwards the packet toward B. [week-02-lecture-02, p. 27]

## Walkthrough

At the source, the host sends a frame to its local switch. The switch forwards it to the router's local interface. The router makes the network-layer forwarding decision and sends the packet through the next network. The destination-side switches then deliver the final local frame to Host B.

The route is therefore a sequence of local link hops joined by a network-layer forwarding decision. Each switch handles the current frame; the router connects the larger network path. [week-02-lecture-02, p. 27]

## Connections and exam relevance

This connects the previous slides: MAC addresses determine each local frame hop, while the destination IP address allows the router to select the path between networks. The red path is one possible route; other routes may exist depending on the network's forwarding information. [week-02-lecture-02, p. 27]

## Check your understanding

Along the red path, which devices make local MAC-based forwarding decisions, and which device makes the inter-network IP-based forwarding decision?

Student response: Switches make local MAC-based decisions, and the router makes the inter-network IP-based decision.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 27]
