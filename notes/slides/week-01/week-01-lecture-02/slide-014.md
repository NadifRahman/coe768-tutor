---
slide_id: "week-01-lecture-02-slide-014"
source_id: "week-01-lecture-02"
page: 14
week: 1
status: teaching
concepts: []
---

# Slide 14

![Original slide 14](../../../public/generated/week-01-lecture-02/slide-014.png)

## Explanation

This slide isolates the part being called the “network” in the course’s component model.

## Walkthrough

The orange outline surrounds the forwarding infrastructure: the switches at the edges and the routers inside the WAN. The hosts—the sender and receiver computers—and the applications running on them are outside the outlined network portion. In this model, the network provides the connectivity and forwarding service between hosts; it is not the applications themselves.

The diagram therefore separates the roles: end hosts generate or consume application data, while switches and routers move that data through the local and wide-area infrastructure. The links are the connections that join these network devices and hosts.

## Connections and exam relevance

This clarifies the earlier hardware-component discussion and the WAN routing example. It also provides a useful abstraction boundary: when studying network operation, focus on how the infrastructure carries traffic between endpoints, while treating endpoint applications as users of that service. [week-01-lecture-02, p. 14]

## Check your understanding

**Check:** In the orange outlined portion, which devices are included in the network, and which parts of the diagram are excluded?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 14]
