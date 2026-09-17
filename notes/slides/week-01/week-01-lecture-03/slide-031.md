---
slide_id: "week-01-lecture-03-slide-031"
source_id: "week-01-lecture-03"
page: 31
week: 1
status: teaching
concepts:
  - router-crosses-link-layer-technologies
---

# Slide 31

![Original slide 31](../../../public/generated/week-01-lecture-03/slide-031.png)

## Explanation

This diagram shows how a Wi-Fi router connects a browser using 802.11 to a web server using Ethernet. The end hosts run the full upper stack: HTTP, TCP, IP, and their local link technology.

The router participates in IP forwarding and has two different link interfaces: an 802.11 interface on the wireless side and an Ethernet interface on the wired side. It does not need to run the browser's HTTP or TCP application conversation to forward the IP packet.

## Walkthrough

On the wireless link, the transmitted unit is an 802.11 frame carrying an IP packet, which carries TCP and HTTP. The router receives that frame, processes the IP layer, and sends the packet onward in a new Ethernet frame. On the wired link, the Ethernet frame carries the same higher-layer IP/TCP/HTTP content toward the server.

Thus, the link-layer wrapper changes at the router, while IP provides continuity between the source and destination and TCP/HTTP remain endpoint protocols.

### Annotation clarification

The annotations are accurate: the browser uses Wi-Fi/802.11, the server uses Ethernet, and the router has separate wireless and wired link interfaces. “The router converts a Wi-Fi frame to an Ethernet frame” is a useful shorthand, but more precisely the router decapsulates the incoming 802.11 frame, processes the IP packet, and encapsulates that packet in a new Ethernet frame. It does not convert Wi-Fi signals directly or alter the HTTP/TCP data. The interface is the router's link-layer connection/adapter on each side, not merely the blue line.

### Dual function of a consumer Wi-Fi router

A consumer Wi-Fi router commonly combines two roles: it bridges Wi-Fi and wired Ethernet devices within the same home LAN, and it routes between that LAN and another IP network such as the Internet/WAN. Different link technologies do not automatically imply different IP networks; bridging can connect them within one IP network.

## Connections and exam relevance

This is the earlier layering principle in a multi-link path: a router can connect different link technologies because IP sits above those link layers.

## Check your understanding

Which layers does the router need to participate in, and which endpoint layers can it simply forward through?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 31]
