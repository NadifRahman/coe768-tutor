---
slide_id: "week-01-lecture-03-slide-024"
source_id: "week-01-lecture-03"
page: 24
week: 1
status: teaching
concepts:
  - protocol-stack-example-http-tcp-ethernet
---

# Slide 24

![Original slide 24](../../../public/generated/week-01-lecture-03/slide-024.png)

## Explanation

This slide supplies the protocols for the design problem from the previous slide:

- HTTP fetches resources such as web pages.
- TCP ensures reliable data transmission.
- Ethernet handles local-area delivery and identifies devices with MAC addresses.

## Walkthrough

When the client requests a page, HTTP creates the application request. TCP carries it reliably, and Ethernet delivers the resulting frames across the local network using MAC addresses. The protocols cooperate through the stack rather than performing the same job.

### Clarification: MAC address versus IP address

A MAC address identifies a network interface on the local link. Switches use MAC addresses to deliver Ethernet frames within that local network. An IP address is a logical network-layer address used by routers to move packets between networks.

For example, if a laptop sends to a remote web server, the packet's destination IP can remain the server's IP across the route. On the laptop's local LAN, however, the Ethernet frame is addressed to the router's MAC address—the next hop. The router removes that local frame and creates a new frame for the next link. Thus, MAC addresses usually change hop by hop, while the destination IP generally stays the remote server's IP.

Concrete example: Laptop `192.168.1.20`/MAC `L` sends to web server `203.0.113.50`/MAC `S`, through a home router and ISP router. On the laptop-to-home-router link, the IP packet is source `192.168.1.20`, destination `203.0.113.50`, while the Ethernet frame is source MAC `L`, destination MAC `home-router-LAN`. On the home-router-to-ISP link, the router creates a new frame with source MAC `home-router-WAN` and destination MAC `ISP-router`, while the IP destination remains `203.0.113.50`. On the final server link, another new frame uses the ISP router's MAC as source and `S` as destination. A home router may also perform NAT, changing the source IP to its public IP; that is separate from the normal hop-by-hop MAC change.

A network interface is a connection point or adapter, not necessarily an entire device. A laptop usually has Wi-Fi and possibly Ethernet interfaces. A router has several interfaces—such as LAN and WAN—each with its own local-link identity. A switch has physical ports and may also have a management interface; ordinary switching forwards frames through ports without acting as an IP-routing hop.

The linked-list analogy is useful if interpreted locally: source and destination IPs usually represent the original sender and final receiver, while each frame's source and destination MACs represent the current link's sender and next recipient. The route is not a prebuilt linked list; each router chooses the next hop from its routing information. Switches may forward the same frame across several ports without creating routed hops.

## Connections and exam relevance

This is a concrete example of mapping requirements to layers: resource access maps to HTTP, reliability maps to TCP, and local-network identification maps to Ethernet.

## Check your understanding

What responsibility does Ethernet add to the HTTP-over-TCP design, and how is a MAC address different from an IP address?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 24]
