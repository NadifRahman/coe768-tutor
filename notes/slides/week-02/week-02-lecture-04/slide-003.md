---
slide_id: "week-02-lecture-04-slide-003"
source_id: "week-02-lecture-04"
page: 3
week: 2
status: understood
concepts: [link-error-control, media-access-control, shared-medium]
---

# Slide 3

![Original slide 3](../../../public/generated/week-02-lecture-04/slide-003.png)

## Explanation

This lecture focuses on two major data-link responsibilities: detecting and handling errors at lower layers, and controlling access to the communication medium. [week-02-lecture-04, p. 3]

## Walkthrough

Noise at the physical layer can corrupt bits, and frames can be lost. The link layer can detect corruption, discard invalid frames, and—when the protocol supports it—request or perform local retransmission.

Media Access Control (MAC) manages who may transmit when multiple hosts share a medium. Without rules, two hosts might transmit simultaneously and interfere with one another. MAC protocols coordinate access to reduce or handle such conflicts. [week-02-lecture-04, p. 3]

## Connections and exam relevance

Be careful with the word “MAC”: it can refer to a hardware/link address, or to the **Media Access Control** part of the link layer that governs access to a shared medium. They are related link-layer concepts but not the same thing. [week-02-lecture-04, p. 3]

## Check your understanding

What two problems does the link layer address in this slide: one involving corrupted/lost frames and one involving multiple hosts sharing a medium?

Student response: The link layer handles local frame errors and coordinates access to a shared medium.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-04, p. 3]
