---
slide_id: "week-01-lecture-01-slide-007"
source_id: "week-01-lecture-01"
page: 7
week: 1
status: teaching
concepts: []
---

# Slide 7

![Original slide 7](../../../public/generated/week-01-lecture-01/slide-007.png)

## Explanation

Another fundamental networking problem is **resource allocation**: several users may need to share one communication medium or channel. The network must decide who can transmit and when.

## Walkthrough

The diagrams show three computers sharing one medium. If A and B transmit at the same time, their signals overlap at the shared channel and produce a **collision**. The receiver may then be unable to interpret either transmission correctly.

The slide names two access-control approaches. Ethernet uses **CSMA/CD** (Carrier Sense Multiple Access with Collision Detection): devices share access and detect when simultaneous transmission causes a collision. Wi‑Fi uses **CSMA/CA** (Carrier Sense Multiple Access with Collision Avoidance): because detecting a collision while transmitting wirelessly is difficult, the protocol emphasizes trying to avoid simultaneous transmissions. [week-01-lecture-01, p. 7]

## Connections and exam relevance

This is an early example of a protocol solving a coordination problem. It connects the physical/shared-medium idea from communications to the network’s responsibility to let many devices communicate fairly and successfully.

## Check your understanding

**Check:** What is the basic problem that CSMA/CD and CSMA/CA are designed to manage?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-01, p. 7]
