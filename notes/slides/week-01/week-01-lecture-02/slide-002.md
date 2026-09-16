---
slide_id: "week-01-lecture-02-slide-002"
source_id: "week-01-lecture-02"
page: 2
week: 1
status: teaching
concepts: []
---

# Slide 2

![Original slide 2](../../../public/generated/week-01-lecture-02/slide-002.png)

## Explanation

Routers and switches both relay messages, but they operate at different scopes in the simplified model used here.

## Walkthrough

A **switch** connects devices within one computer network, such as several PCs in the same LAN. A **router** connects different computer networks and chooses how traffic moves between them. In the diagram, PCs A–C connect to the left switch, and PCs D–F connect to the right switch. The router links those two local networks.

If PC A sends data to PC B, the left switch can forward it within the same local network. If PC A sends data to PC D, the traffic must cross the router because the destination is on another network. In both cases the devices relay messages, but the router’s job includes crossing network boundaries.

## Connections and exam relevance

This distinction gives a practical meaning to the earlier LAN/MAN/WAN discussion: switches commonly build local networks, while routers interconnect separate networks. It is also useful when tracing a packet hop by hop. [week-01-lecture-02, p. 2]

## Check your understanding

**Check:** In the diagram, why can traffic from PC A to PC B stay with the left switch, while traffic from PC A to PC D must pass through the router?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 2]
