---
slide_id: "week-02-lecture-03-slide-003"
source_id: "week-02-lecture-03"
page: 3
week: 2
status: understood
concepts: [bit-error-rate, message-latency, fiber-wireless-comparison]
---

# Slide 3

![Original slide 3](../../../public/generated/week-02-lecture-03/slide-003.png)

## Explanation

Error rate is the percentage of received bits that contain errors relative to the total number of received bits. Message latency, or delay, is the time required to send a message across a communication channel. [week-02-lecture-03, p. 3]

## Walkthrough

The slide contrasts media: fiber generally has a very low error rate, while wireless channels are more exposed to interference and therefore may have higher error rates. If errors occur, error detection and retransmission mechanisms are needed to recover the intended data.

Latency is separate from bit rate. A link can transmit many bits per second yet still have noticeable delay before a message reaches the other side. Latency can include transmission time, propagation time, processing, and queueing. [week-02-lecture-03, p. 3]

## Connections and exam relevance

These metrics describe different channel qualities: bandwidth/bit rate describe capacity or speed, error rate describes correctness, and latency describes time-to-arrival. A network can have high bandwidth but poor latency, or low error rate but long propagation delay. [week-02-lecture-03, p. 3]

## Check your understanding

What is the difference between error rate and latency: does one measure incorrect bits, elapsed time, or both?

Student response: Error rate measures incorrect bits, while latency measures elapsed time.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-03, p. 3]
