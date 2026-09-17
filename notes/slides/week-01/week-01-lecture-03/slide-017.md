---
slide_id: "week-01-lecture-03-slide-017"
source_id: "week-01-lecture-03"
page: 17
week: 1
status: teaching
concepts:
  - network-layering-and-modularity
---

# Slide 17

![Original slide 17](../../../public/generated/week-01-lecture-03/slide-017.png)

## Explanation

An intermediate network layer can hide the details of the transmission medium. Applications and higher-level protocols can use a common interface whether the data travels over copper, fiber, or wireless media.

This gives two major advantages: hiding details and reusing functionality. A common lower-layer function can be shared by many upper-layer applications or protocols.

## Walkthrough

For example, a web application does not need separate application logic for Wi-Fi, Ethernet cable, and fiber. It uses the layer's interface, and the lower layers select and manage the appropriate medium.

## Connections and exam relevance

This is abstraction in practice: upper layers depend on what a lower layer provides, not on how that lower layer implements it.

## Check your understanding

What are the two advantages of layering emphasized on this slide?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 17]
