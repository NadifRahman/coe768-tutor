---
slide_id: "week-02-lecture-03-slide-005"
source_id: "week-02-lecture-03"
page: 5
week: 2
status: understood
concepts: [propagation-delay, signal-speed, message-latency-formula]
---

# Slide 5

![Original slide 5](../../../public/generated/week-02-lecture-03/slide-005.png)

## Explanation

Propagation delay is the time for the signal to travel through the medium from the sender to the receiver. It depends on the link length and the propagation speed of the medium, not on the packet size. [week-02-lecture-03, p. 5]

## Walkthrough

The formula is:

`D = link length / propagation speed`

For many wired media, the signal travels at roughly two-thirds of the speed of light. Wireless propagation through air is close to the speed of light. The slide's simplified message-latency formula is:

`message latency = M/R + D`

That combines transmission delay (`M/R`) with propagation delay (`D`). In a real multi-hop network, processing and queueing delays must also be included. [week-02-lecture-03, p. 5]

## Connections and exam relevance

Transmission delay answers “how long to put all bits onto the link?” Propagation delay answers “how long does the signal take to travel through the link?” A high bit rate reduces transmission delay, but it does not necessarily reduce propagation delay; propagation mainly depends on distance and signal speed. [week-02-lecture-03, p. 5]

## Check your understanding

If a link is 200 km long and the signal travels at 200,000 km/s, what is the propagation delay across that link?

Student response: 1 ms.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-03, p. 5]
