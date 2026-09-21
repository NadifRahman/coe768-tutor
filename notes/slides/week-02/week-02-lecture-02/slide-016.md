---
slide_id: "week-02-lecture-02-slide-016"
source_id: "week-02-lecture-02"
page: 16
week: 2
status: understood
concepts: [device-layer-roles, addressing-by-layer, host-router-switch]
---

# Slide 16

![Original slide 16](../../../public/generated/week-02-lecture-02/slide-016.png)

## Explanation

Layering also helps us understand what different network devices do and which addressing scheme they use. In the course's practical five-layer view, hosts participate at the higher layers, routers operate at the Internet/IP layer, switches operate at the data-link/MAC layer, and hubs or repeaters operate at the physical layer. [week-02-lecture-02, p. 16]

## Walkthrough

The table summarizes the association:

- Application layer → host applications
- Transport layer → hosts, using TCP/UDP ports
- Internet layer → routers and hosts, using IP addresses
- Data-link layer → switches and hosts, using MAC addresses
- Physical layer → hubs, repeaters, and hosts, using signals rather than addresses

This is a reasoning tool: a host participates in all layers, while a switch or router is specialized around particular responsibilities. [week-02-lecture-02, p. 16]

## Connections and exam relevance

This connects the device to the identifier it uses for forwarding: switches make local forwarding decisions using link-layer/MAC information, while routers make inter-network forwarding decisions using IP information. Transport ports identify applications at the host rather than identifying physical devices. [week-02-lecture-02, p. 16]

## Check your understanding

Which device primarily uses MAC addresses to forward within a local network, and which device primarily uses IP addresses to forward between networks?

Student response: A switch uses MAC addresses for local forwarding, and a router uses IP addresses for forwarding between networks.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 16]
