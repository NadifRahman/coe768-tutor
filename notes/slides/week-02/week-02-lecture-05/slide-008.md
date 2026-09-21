---
slide_id: "week-02-lecture-05-slide-008"
source_id: "week-02-lecture-05"
page: 8
week: 2
status: understood
concepts: [layered-error-detection, local-retransmission, end-to-end-recovery, packet-drop]
---

# Slide 8

![Original slide 8](../../../public/generated/week-02-lecture-05/slide-008.png)

## Explanation

Yes, multiple layers can have their own checks, but they do not form one single error-handling ladder. Each layer checks the unit it owns and follows that protocol’s recovery rules. A lower layer may discard a corrupted frame or retransmit it locally; if recovery fails, the higher layer may eventually observe a missing or delayed packet and handle it independently. [week-02-lecture-05, p. 8]

## Walkthrough

The diagram shows the same upper-layer data being encapsulated into a TCP packet, then an IP packet, and finally a link-layer frame. Checks happen at different scopes:

- A checksum can detect corruption in the packet or segment covered by that checksum. A bad packet may be dropped.
- Ethernet’s CRC checks the local frame. If the CRC is wrong, Ethernet discards the frame. Ethernet itself may not retransmit it, so TCP may later notice the missing data and retransmit end-to-end.
- 802.11 commonly performs local retransmission when a frame is not acknowledged, so the wireless link can repair a loss before TCP needs to react.

Therefore, a low-level retransmission is usually **hop-by-hop/local**, while TCP retransmission is **end-to-end** between the original sender and receiver. A frame error does not get “passed upward” as a corrupted frame; it is normally rejected. What may reach the higher layer is a delay, a missing packet, or eventually a transport timeout. [week-02-lecture-05, p. 8]

## Connections and exam relevance

Layering can create redundant protection. That is intentional: local recovery is faster and avoids wasting an entire end-to-end retransmission, while TCP still protects delivery across all links in the path. UDP does not provide TCP-style reliable retransmission, so an application using UDP must tolerate loss or implement its own recovery if needed. [week-02-lecture-05, p. 8]

## Check your understanding

If an Ethernet frame fails its CRC and is dropped, does TCP immediately see the corrupted bytes, or does it usually see a missing/delayed segment instead?

Student response: TCP does not receive the corrupted bytes; it usually sees a missing or delayed segment after lower-layer handling.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-05, p. 8]
