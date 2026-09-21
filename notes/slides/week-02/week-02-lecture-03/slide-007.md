---
slide_id: "week-02-lecture-03-slide-007"
source_id: "week-02-lecture-03"
page: 7
week: 2
status: understood
concepts: [multi-hop-delay, store-and-forward, delay-equivalence]
---

# Slide 7

![Original slide 7](../../../public/generated/week-02-lecture-03/slide-007.png)

## Explanation

This example extends the delay formulas to two equal links, A–B and B–C. Each link has length `x`, bit rate `R`, and propagation speed `y`. A message of `L` bits travels from A to C, with only transmission and propagation delays considered. [week-02-lecture-03, p. 7]

## Walkthrough

The total propagation distance is `2x`, so:

`d_prop = 2x/y`

Assuming store-and-forward transmission at B, the message is transmitted across both links, so:

`d_trans = 2L/R`

If the two delays are equal:

`2x/y = 2L/R`

The factors of 2 cancel, giving:

`x = Ly/R`

Using `y = 2×10⁸ m/s`, `L = 1000 bits`, and `R = 100 kbps`, the result is `x = 2×10⁶ m = 2000 km`. [week-02-lecture-03, p. 7]

## Connections and exam relevance

The example highlights that propagation delay grows with distance, while transmission delay grows with message size and decreases with bit rate. The two-hop transmission total assumes the packet must be fully received at B before being transmitted onto the B–C link. [week-02-lecture-03, p. 7]

## Check your understanding

Why is the total propagation delay `2x/y`, while the total transmission delay is `2L/R` in this two-link example?

Student response: There are two links, so the signal propagates across two distances and the message is transmitted over both links.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-03, p. 7]
