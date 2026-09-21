---
slide_id: "week-02-lecture-02-slide-018"
source_id: "week-02-lecture-02"
page: 18
week: 2
status: understood
concepts: [mac-address, network-interface, router-interface]
---

# Slide 18

![Original slide 18](../../../public/generated/week-02-lecture-02/slide-018.png)

## Explanation

A MAC address is assigned to a network interface that participates in a local-area link such as Ethernet, Wi-Fi, or Bluetooth. Computers, servers, and phones have MAC addresses through their network adapters. A router can have MAC addresses on its LAN-connected interfaces because those interfaces participate in local links. [week-02-lecture-02, p. 18]

## Walkthrough

The important unit is the **network interface**, not necessarily the whole device. A laptop with Ethernet and Wi-Fi can have a different MAC address for each interface. A router may have one MAC address per relevant Ethernet/Wi-Fi interface. MAC addresses are used for local-link delivery and are not the same as IP addresses, which identify network-layer endpoints. [week-02-lecture-02, p. 18]

## Connections and exam relevance

The slide says a switch does not need to have a MAC address for its basic switching function: it forwards frames based on the MAC addresses in those frames. In practice, managed switches often have a management interface and may have MAC addresses, but that is not required for the conceptual forwarding role shown here. [week-02-lecture-02, p. 18]

## Check your understanding

If a router has three Ethernet interfaces connected to three different local networks, should we expect one MAC address total or a MAC address associated with each interface?

Student response: We expect three MAC addresses, one associated with each Ethernet interface.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 18]
