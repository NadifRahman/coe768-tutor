---
slide_id: "week-02-lecture-05-slide-002"
source_id: "week-02-lecture-05"
page: 2
week: 2
status: understood
concepts: [single-bit-error, multiple-bit-error, burst-error, check-bits]
---

# Slide 2

![Original slide 2](../../../public/generated/week-02-lecture-05/slide-002.png)

## Explanation

Transmission errors can be classified by how many bits are corrupted and whether the corrupted bits are adjacent. The slide introduces three patterns: single-bit, multiple-bit, and burst errors. It then introduces **check bits**, also called an error-detection code, which add redundancy so the receiver can recognize that an error occurred. [week-02-lecture-05, p. 2]

## Walkthrough

**Single-bit error:** exactly one bit changes, such as `0` becoming `1`.

**Multiple-bit error:** two or more bits change, but the changed bits are not necessarily next to each other.

**Burst error:** two or more consecutive bits are corrupted. “Burst” describes the pattern, not necessarily the exact number of bits.

To handle these cases, the sender adds check bits to the message. The receiver recomputes or checks the relevant rule; if the check fails, it knows the message was corrupted. The slide also notes that this general idea can be used by different layers, although this lecture is focusing on its role at the link layer. [week-02-lecture-05, p. 2]

## Connections and exam relevance

Do not confuse **error detection** with **error correction**. A check may tell the receiver that corruption occurred without telling it how to reconstruct the original data. Recovery may require retransmission or a stronger code. [week-02-lecture-05, p. 2]

## Check your understanding

What distinguishes a multiple-bit error from a burst error?

Student response: A burst error affects consecutive bits, while a multiple-bit error can affect separated bits.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-05, p. 2]
