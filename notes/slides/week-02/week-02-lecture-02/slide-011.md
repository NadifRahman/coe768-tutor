---
slide_id: "week-02-lecture-02-slide-011"
source_id: "week-02-lecture-02"
page: 11
week: 2
status: understood
concepts: [router-forwarding, hop-by-hop-link-headers, end-to-end-ip-addresses]
---

# Slide 11

![Original slide 11](../../../public/generated/week-02-lecture-02/slide-011.png)

## Explanation

This slide shows how a router forwards a packet from a source host to a destination host across two networks. The router removes the incoming data-link header and creates a new data-link header for the outgoing link. The packet's higher-layer contents continue through the router. [week-02-lecture-02, p. 11]

## Walkthrough

On the first link, the frame uses the source host's MAC address and the router's first-interface MAC address. On the second link, the frame uses the router's second-interface MAC address and the destination host's MAC address. Therefore, the MAC addresses change at the router because they identify the endpoints of the current local link.

By contrast, the source and destination IP addresses identify the overall endpoints, and the transport ports identify the application endpoints. Those higher-layer values remain associated with the end-to-end communication while each local link gets a new frame header. [week-02-lecture-02, p. 11]

## Connections and exam relevance

This is the practical meaning of “the data link layer is local” and “the network layer spans multiple networks.” A router operates at the IP/network layer to choose the next path, but it must rebuild the link-layer frame for each outgoing interface. The same application data is therefore carried in a sequence of hop-specific frames. [week-02-lecture-02, p. 11]

## Check your understanding

When a packet crosses a router, which addresses change: the MAC addresses, the IP addresses, or both? Explain why.

Student response: MAC addresses change at each local hop because they identify the current link endpoints; IP addresses remain the end-to-end source and destination in this example.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 11]
