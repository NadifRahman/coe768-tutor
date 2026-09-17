---
slide_id: "week-01-lecture-03-slide-022"
source_id: "week-01-lecture-03"
page: 22
week: 1
status: teaching
concepts:
  - protocol-stack-and-layer-interfaces
---

# Slide 22

![Original slide 22](../../../public/generated/week-01-lecture-03/slide-022.png)

## Explanation

In a protocol stack, each layer has a neighboring layer above and below it. The neighboring layers interact through an interface: the lower layer provides a service, and the upper layer uses that service. Matching layers on two hosts follow the same protocol conceptually.

## Walkthrough

In the diagram, data flows down Host 1's stack, across wired or wireless physical media, and up Host 2's stack. Protocol X runs at the upper layer, Protocol Y in the middle, and Protocol Z near the physical medium.

Only adjacent layers directly interact within a host. The bottom layer converts the message into physical signals—such as electrical, optical, or radio signals—that travel across the medium.

## Connections and exam relevance

The stack extends the two-layer idea from the previous slide. Interfaces support vertical interaction on one host, while the same protocol at corresponding layers defines peer interaction between hosts.

## Check your understanding

What is the role of the interface between two neighboring layers?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 22]
