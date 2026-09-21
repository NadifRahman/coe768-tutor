---
slide_id: "week-02-lecture-03-slide-004"
source_id: "week-02-lecture-03"
page: 4
week: 2
status: understood
concepts: [transmission-delay, data-rate, transmission-delay-formula]
---

# Slide 4

![Original slide 4](../../../public/generated/week-02-lecture-03/slide-004.png)

## Explanation

Transmission delay is the time required to push all bits of a packet from the host onto the transmission medium. It is calculated as data size divided by bit rate: `d_trans = M/R`, where M is the packet size in bits and R is the bit rate in bits per second. [week-02-lecture-03, p. 4]

## Walkthrough

In the slide's example, the packet contains 30 bits and the link can transmit 5 bits per second. Therefore:

`d_trans = 30 bits / (5 bits/s) = 6 s`

After 6 seconds, all 30 bits have been placed onto the medium. This is transmission delay; it is distinct from propagation delay, which is the time for the signal to travel through the medium after it has been transmitted. [week-02-lecture-03, p. 4]

## Connections and exam relevance

For a fixed packet size, increasing the bit rate decreases transmission delay. For a fixed bit rate, a larger packet takes longer to place onto the link. The formula concerns serialization onto the link, not queueing, processing, or signal propagation. [week-02-lecture-03, p. 4]

## Check your understanding

If a 1000-bit packet is sent over a 100-bit/s link, what is its transmission delay?

Student response: 10 seconds.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-03, p. 4]
