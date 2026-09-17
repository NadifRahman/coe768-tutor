---
slide_id: "week-01-lecture-03-slide-027"
source_id: "week-01-lecture-03"
page: 27
week: 1
status: teaching
concepts:
  - tcp-http-exchange-with-mac-and-ip
---

# Slide 27

![Original slide 27](../../../public/generated/week-01-lecture-03/slide-027.png)

## Explanation

This example combines the earlier ideas: a client contacts a web server through a hub. The client and server have both IP addresses and MAC addresses. The application exchange uses HTTP, while TCP provides the connection and reliable transport underneath.

## Walkthrough

The message sequence is:

1. Client sends TCP `SYN`.
2. Server replies `SYN-ACK`.
3. Client sends `ACK`.
4. Client sends an HTTP request.
5. Server acknowledges it with TCP `ACK`.
6. Server sends the HTTP response.
7. Client acknowledges the response.

The hub is a shared local-medium device: it repeats the incoming signal to its connected ports. The Ethernet frame still carries source and destination MAC addresses, while the IP addresses identify the client and server at the network layer.

Because a hub repeats the signal to every port, every attached network interface can physically observe the frame. Each NIC checks the destination MAC: the intended device accepts and processes it, while other devices normally discard it. Broadcast and some multicast frames are intentionally accepted by multiple devices. A switch reduces this unnecessary sharing by forwarding a known unicast frame only through the appropriate port.

An Ethernet frame is the link-layer container for one local transmission. It typically contains a destination MAC, source MAC, a type/length field, a payload containing an IP packet, and an FCS trailer used to detect transmission errors. Conceptually: `Ethernet header [IP packet [TCP segment [HTTP data]]] Ethernet trailer`. A router removes the old link-layer frame and creates a new frame for the next link; switches normally forward the frame without changing its MAC addresses.

## Connections and exam relevance

This links the protocol stack to a tangible LAN: HTTP is the application conversation, TCP is the reliable transport, IP identifies the network endpoints, and Ethernet/MAC handles local delivery.

## Check your understanding

Which protocol is responsible for the `SYN`, `SYN-ACK`, and acknowledgment messages, and which protocol carries the web request?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 27]
