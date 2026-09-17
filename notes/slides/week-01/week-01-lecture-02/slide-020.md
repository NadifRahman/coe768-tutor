---
slide_id: "week-01-lecture-02-slide-020"
source_id: "week-01-lecture-02"
page: 20
week: 1
status: teaching
concepts: []
---

# Slide 20

![Original slide 20](../../../public/generated/week-01-lecture-02/slide-020.png)

## Explanation

Traceroute discovers a path by sending a sequence of probe messages with increasing TTL values.

## Walkthrough

Suppose the destination is five hops away. The source first sends a probe with TTL 1. Router 1 decrements it to zero, discards the probe, and returns ICMP Time Exceeded; the source records Router 1. The source then sends a new probe with TTL 2. Router 1 reduces it to 1, Router 2 reduces it to zero, and the source records Router 2. The process repeats with TTL 3 and 4 to discover Routers 3 and 4.

With TTL 5, the probe survives all four routers and reaches the destination, which sends a response. The source now has the ordered hop list and a timing measurement for each hop. If the destination or route cannot be reached, an ICMP Destination Unreachable response may end the attempt instead.

## Connections and exam relevance

This is the step-by-step mechanism behind the traceroute purpose introduced on Slide 17. It uses TTL as a controlled limit to reveal one additional router per probe. [week-01-lecture-02, p. 20]

## Check your understanding

**Check:** Why does traceroute send probes with TTL values of 1, then 2, then 3, instead of sending only one probe with a large TTL?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 20]
