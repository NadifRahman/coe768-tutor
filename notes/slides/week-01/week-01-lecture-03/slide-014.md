---
slide_id: "week-01-lecture-03-slide-014"
source_id: "week-01-lecture-03"
page: 14
week: 1
status: teaching
concepts:
  - network-layering-and-modularity
---

# Slide 14

![Original slide 14](../../../public/generated/week-01-lecture-03/slide-014.png)

## Explanation

To send Mia's electronic mail to Richard, the network still needs layering. The problem is decomposed into manageable subproblems, and each network layer is responsible for different functions or services.

Those services are implemented through protocols: agreed rules that specify how each layer performs its job and communicates with the corresponding layer on another host.

## Walkthrough

Instead of designing one giant procedure for email delivery, the system separates tasks such as application-level email handling, reliable transport, addressing and routing, and link-level transmission. Each layer provides a service to the layer above it and uses the service below it.

## Connections and exam relevance

This is the motivation for the protocol stack introduced later in the course. Modularity allows one layer's implementation to change without redesigning every other layer, as long as its service interface remains compatible.

## Check your understanding

Why do computer networks use multiple layers and protocols instead of one large procedure for sending email?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 14]
