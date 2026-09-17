---
slide_id: "week-01-lecture-03-slide-023"
source_id: "week-01-lecture-03"
page: 23
week: 1
status: teaching
concepts:
  - designing-a-protocol-stack
---

# Slide 23

![Original slide 23](../../../public/generated/week-01-lecture-03/slide-023.png)

## Explanation

This slide presents a protocol-stack design problem. A client must fetch web pages from a server through a hub, and the transmission must be reliable.

The requirements imply at least an application protocol for web pages and a transport protocol for reliability. The lower layers then provide local delivery over the hub and its physical medium.

## Walkthrough

The natural design is:

- Application layer: HTTP, to request and receive web pages.
- Transport layer: TCP, to provide reliable, ordered delivery.
- Lower link/physical layers: the local network and hub/medium mechanisms that carry the bits between client and server.

The exact number of layers depends on how finely the design separates link and physical responsibilities. The important method is to derive each layer from a required service rather than choosing layers arbitrarily.

## Connections and exam relevance

This applies the previous slides: HTTP uses TCP through an interface, and TCP uses lower-layer services. The next step is to identify the protocols that implement those services.

## Check your understanding

Which protocol handles web-page fetching, and which protocol provides reliable transmission?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 23]
