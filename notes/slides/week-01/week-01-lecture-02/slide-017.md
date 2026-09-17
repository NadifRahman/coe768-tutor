---
slide_id: "week-01-lecture-02-slide-017"
source_id: "week-01-lecture-02"
page: 17
week: 1
status: teaching
concepts: []
---

# Slide 17

![Original slide 17](../../../public/generated/week-01-lecture-02/slide-017.png)

## Explanation

**Traceroute** is a network diagnostic tool that reveals the path data takes from a source to a destination.

## Walkthrough

Traceroute reports the IP addresses of routers encountered along the route and measures the time for each hop. A **hop** is one router crossing between the source and destination. The timing is generally a round-trip latency: how long it takes for a probe to reach that hop and for a response to return.

This makes the network cloud partially observable. If one hop has much higher latency than neighboring hops, or stops responding, it can provide a clue about where delay or a connectivity problem occurs. A missing response does not automatically prove that the router is broken; some routers or firewalls simply do not answer diagnostic probes.

## Connections and exam relevance

Traceroute complements Nmap and Wireshark from earlier slides: Nmap discovers hosts and services, Wireshark inspects traffic, and traceroute shows a route and per-hop timing. It directly demonstrates the hop-by-hop forwarding described on Slide 13. [week-01-lecture-02, p. 17]

## Check your understanding

**Check:** What two kinds of information does traceroute report about the path from a source to a destination?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 17]
