---
slide_id: "week-02-lecture-02-slide-026"
source_id: "week-02-lecture-02"
page: 26
week: 2
status: understood
concepts: [ip-address, logical-location, router-interface-addressing]
---

# Slide 26

![Original slide 26](../../../public/generated/week-02-lecture-02/slide-026.png)

## Explanation

An IP address is a numerical network-layer label, such as `192.0.2.1`, associated with an interface on an IP network. It serves two related purposes: identifying the endpoint/interface and indicating its logical location in the network. Routers use this location information to forward packets. [week-02-lecture-02, p. 26]

## Walkthrough

Unlike a MAC address, which is mainly a local-link identifier, an IP address is structured so that routing can use network prefixes and host/interface portions. A router has interfaces connected to different networks, and each interface normally has an IP address belonging to its attached network. The image labels LAN, WAN, and management connections to illustrate these different interfaces. [week-02-lecture-02, p. 26]

## Connections and exam relevance

This explains why IP is suitable for internetworking: the address is not merely a permanent hardware label; it also conveys where the interface is located within the network topology. MAC addresses help deliver a frame on the current link, while IP addresses help move a packet toward a destination across multiple networks. [week-02-lecture-02, p. 26]

## Check your understanding

Why does an IP address need to provide both an endpoint identity and a logical network location?

Student response: It identifies the endpoint and provides location information that routers use to move packets toward the destination.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 26]
