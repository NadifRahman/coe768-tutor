---
slide_id: "week-01-lecture-03-slide-028"
source_id: "week-01-lecture-03"
page: 28
week: 1
status: teaching
concepts:
  - tcp-control-segments-and-ethernet-encapsulation
---

# Slide 28

![Original slide 28](../../../public/generated/week-01-lecture-03/slide-028.png)

## Explanation

The TCP connection messages—SYN, SYN-ACK, and ACK—do not carry HTTP or other application data. They contain TCP control information, primarily represented by a TCP header, and are then encapsulated inside Ethernet frames for local transmission.

## Walkthrough

The diagram shows the stack at the browser and server and the data units crossing the Ethernet link. During the handshake, the TCP layer exchanges control-only segments. Ethernet wraps each TCP segment for delivery, but there is no application payload yet because the HTTP request is sent only after the TCP connection is established.

The Ethernet header is needed because TCP's segment still needs a local-link wrapper. It supplies source and destination MAC addresses for the current LAN and a type field identifying the payload, while the Ethernet trailer supports frame-level error detection. IP handles broader routing and TCP handles transport control; Ethernet handles this particular link.

Diagram walkthrough: the browser's TCP layer creates a control segment such as `SYN`, containing TCP control fields but no application data. That segment moves down to the browser's Ethernet layer. Ethernet wraps it as a frame: `[Ethernet header [TCP header] Ethernet trailer]`. The frame crosses the wired or wireless link. The server's Ethernet layer checks the frame's local information, removes the Ethernet wrapper, and passes the TCP segment upward to the server's TCP layer. The server TCP layer reads `SYN` and creates a `SYN-ACK`; the same wrapping and unwrapping happens in the reverse direction. The diagram shows only TCP headers because this is the handshake stage, before HTTP data is sent.

## Connections and exam relevance

This distinguishes transport control messages from application messages: TCP can communicate to establish reliability before HTTP begins sending its web data.

## Check your understanding

Why does a TCP SYN segment contain no HTTP application data?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 28]
