---
slide_id: "week-02-lecture-03-slide-006"
source_id: "week-02-lecture-03"
page: 6
week: 2
status: understood
concepts: [latency-calculation, unit-conversion, transmission-plus-propagation]
---

# Slide 6

![Original slide 6](../../../public/generated/week-02-lecture-03/slide-006.png)

## Explanation

This example combines propagation delay and transmission delay to calculate message latency. The given values are propagation delay `D = 10 ms`, bit rate `R = 40 kbps`, and message size `M = 2000 bytes`. [week-02-lecture-03, p. 6]

## Walkthrough

First convert bytes to bits:

`2000 bytes × 8 = 16,000 bits`

Then calculate transmission delay:

`M/R = 16,000 / 40,000 = 0.4 s = 400 ms`

Finally add propagation delay:

`message latency = 400 ms + 10 ms = 410 ms`

The important exam habit is to convert all quantities into compatible units before adding them. [week-02-lecture-03, p. 6]

## Connections and exam relevance

This example reinforces that bytes must be converted to bits because the rate is given in bits per second. It also shows that the total latency is not just propagation delay: the sender first needs time to serialize the entire message onto the link. [week-02-lecture-03, p. 6]

## Check your understanding

Using the same values, what is the transmission delay alone before adding the 10 ms propagation delay?

Student response: 400 ms.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-03, p. 6]
