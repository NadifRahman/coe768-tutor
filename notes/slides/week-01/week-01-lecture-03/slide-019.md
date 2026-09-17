---
slide_id: "week-01-lecture-03-slide-019"
source_id: "week-01-lecture-03"
page: 19
week: 1
status: teaching
concepts:
  - tcp-reliable-data-transmission
---

# Slide 19

![Original slide 19](../../../public/generated/week-01-lecture-03/slide-019.png)

## Explanation

TCP provides the reliable-data-transmission service. In the normal case, data arrives without loss. If data is lost along the way, TCP gives the endpoints a way to identify the missing data and retransmit it.

## Walkthrough

For example, a sender transmits segments and the receiver acknowledges the data it has received. If an acknowledgment indicates a gap—or does not arrive in time—the sender can resend the missing segment. TCP also uses sequence numbers so the receiver can place data in the correct order.

## Connections and exam relevance

This is why applications such as HTTP can rely on TCP for dependable delivery instead of implementing retransmission themselves. UDP does not provide this built-in recovery.

## Check your understanding

If one TCP segment is lost, what mechanism allows the sender to deliver that data again?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 19]
