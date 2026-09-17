---
slide_id: "week-01-lecture-02-slide-018"
source_id: "week-01-lecture-02"
page: 18
week: 1
status: teaching
concepts: []
---

# Slide 18

![Original slide 18](../../../public/generated/week-01-lecture-02/slide-018.png)

## Explanation

The **Internet Control Message Protocol (ICMP)** supports diagnostic messages used to test whether a destination can be reached. The common `ping` command sends an ICMP message to a destination IP address and waits for a response.

## Walkthrough

The diagram shows a ping from SRC to destination 10.1.1.1 through four routers. The response time is recorded as **latency**, usually the round-trip time from source to destination and back.

The message also carries a **TTL** (time to live) value. Each forwarding device decreases TTL by one. This prevents a message from circulating forever if routing loops occur. In the example, the initial TTL is 64; after crossing four routers, the remaining value would be 60 if it reaches the destination. If TTL reaches zero before delivery, the network returns a TTL-exceeded message to the source.

For a running example, imagine the source executes `ping 10.1.1.1` with an initial TTL of 64. The ICMP request travels through Router 1, Router 2, Router 3, and Router 4, so its TTL becomes 60 before reaching the destination. The destination sends a reply back, and the source measures how long the complete trip took. If the request’s TTL had been only 3, it would reach Router 3 with no remaining lifetime for the next hop, and the source would receive a TTL-exceeded diagnostic instead of a successful reply.

## Connections and exam relevance

Ping and traceroute both use diagnostic exchanges to reveal network behavior. Ping focuses on reachability and round-trip latency, while traceroute varies or observes hop limits to identify intermediate routers and per-hop timing. [week-01-lecture-02, p. 18]

## Check your understanding

**Check:** What happens to the TTL value as a ping message passes through routers, and why is that useful?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 18]
