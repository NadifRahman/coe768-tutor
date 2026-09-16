---
slide_id: "week-01-lecture-02-slide-013"
source_id: "week-01-lecture-02"
page: 13
week: 1
status: teaching
concepts: []
---

# Slide 13

![Original slide 13](../../../public/generated/week-01-lecture-02/slide-013.png)

## Explanation

This slide shows how a WAN can connect several LANs and how routers move data toward its destination.

## Walkthrough

LAN 1 contains the sender and its switch, LAN 2 contains the receiver and its switch, and LAN 3 is another local network. The WAN cloud contains multiple interconnected routers, giving traffic possible paths across the larger network.

The message is represented as containing a sender IP address, a receiver or destination IP address, and data. Each router examines the destination IP address and chooses the next hop—the next router or network device to which it should forward the data. The router does not need to deliver the message directly to the final computer in one step; it forwards the message hop by hop until it reaches the destination LAN.

## Connections and exam relevance

This is the packet-forwarding version of the WAN idea from Slide 12. It also connects routers to the addressing and routing mechanisms that allow separate LANs to communicate. Multiple paths through the WAN support resilience if one route becomes unavailable. [week-01-lecture-02, p. 13]

## Check your understanding

**Check:** What piece of information does each router use to decide the next hop for a message?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 13]
