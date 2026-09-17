---
slide_id: "week-01-lecture-02-slide-021"
source_id: "week-01-lecture-02"
page: 21
week: 1
status: teaching
concepts: []
---

# Slide 21

![Original slide 21](../../../public/generated/week-01-lecture-02/slide-021.png)

## Explanation

This slide shows a real-looking traceroute output to `google.com` and maps the listed hops onto a router diagram.

## Walkthrough

The command resolves `google.com` to a destination IP and reports a maximum hop limit and probe size. Each numbered row is one hop. The first field is a router name or label, the address in parentheses is its IP address, and the following three values are measured round-trip times for separate probes.

In this example, hop 1 is the local gateway, later hops belong to intermediate provider networks, and the final row reaches the destination address. The diagram below visualizes the observed path through the larger possible network. Latency can vary between probes, and a traceroute path is not necessarily permanent: routing can change, and some hops may be hidden or fail to respond.

## Connections and exam relevance

This example combines destination addressing, hop-by-hop routing, TTL, ICMP responses, and latency measurement from the previous slides. It shows what a diagnostic tool can reveal about the otherwise abstract network cloud. [week-01-lecture-02, p. 21]

## Check your understanding

**Check:** In one numbered traceroute row, what do the hop number, IP address, and three time values represent?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 21]
