---
slide_id: "week-01-lecture-01-slide-008"
source_id: "week-01-lecture-01"
page: 8
week: 1
status: teaching
concepts: []
---

# Slide 8

![Original slide 8](../../../public/generated/week-01-lecture-01/slide-008.png)

## Explanation

The third fundamental problem is **flow control**: ensuring that a sender does not deliver data faster than the receiver can process or store it. Without flow control, a receiver’s buffer can overflow and data can be lost.

## Walkthrough

In the real-time audio/video example, the sender’s audio and video sources are encoded, transmitted through the network cloud, decoded at the receiver, and sent to playback. If the sender produces data faster than the receiver can handle it, data accumulates and may overflow the receiver’s capacity.

The slide gives two solutions at different scopes. For **nodes in the network**, the data-link layer can use **stop-and-wait**: send a unit, wait for an acknowledgement or appropriate response, then continue. For **hosts**, the transport layer can use a **sliding window**, allowing a controlled amount of data to be in flight while limiting how much unprocessed data can arrive at once.

## Connections and exam relevance

Flow control complements reliability and resource allocation: reliability handles errors and failures, resource allocation handles competing senders, and flow control matches the sender’s rate to the receiver’s capacity. The distinction between data-link-layer and transport-layer mechanisms previews the layered architecture used throughout the course. [week-01-lecture-01, p. 8]

## Check your understanding

**Check:** What problem occurs if a sender transmits faster than the receiver can process, and how does flow control prevent it?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-01, p. 8]
