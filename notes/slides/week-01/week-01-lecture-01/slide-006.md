---
slide_id: "week-01-lecture-01-slide-006"
source_id: "week-01-lecture-01"
page: 6
week: 1
status: teaching
concepts: []
---

# Slide 6

![Original slide 6](../../../public/generated/week-01-lecture-01/slide-006.png)

## Explanation

One fundamental network problem is **reliability**: the ability to recover from errors or failures. Networks cannot assume that every transmission will arrive unchanged or that every device will remain operational.

## Walkthrough

There are two examples. First, a message can be corrupted while crossing the network. Code can add information that lets the receiver detect an error; if an error is detected, the system can discard the damaged data or request a retransmission. Detection is different from correction: detection notices that something is wrong, while correction or retransmission restores the intended data.

Second, a router may fail, making one path to a website unavailable. A network can improve reliability through multiple routes and routing decisions that avoid the failed router. The overall idea is redundancy: do not depend on one perfect transmission or one device.

## Connections and exam relevance

Reliability is a core design concern behind later topics such as error detection, retransmission, routing, and alternate paths. It also explains why the Internet can continue operating even when individual links or routers fail. [week-01-lecture-01, p. 6]

## Check your understanding

**Check:** If a receiver detects that a message was corrupted, what does error-detection code tell it, and what additional action might be needed to obtain the correct message?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-01, p. 6]
