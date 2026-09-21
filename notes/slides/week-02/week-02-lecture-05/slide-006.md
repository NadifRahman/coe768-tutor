---
slide_id: "week-02-lecture-05-slide-006"
source_id: "week-02-lecture-05"
page: 6
week: 2
status: understood
concepts: [ip-header-checksum, tcp-checksum, error-check-cost, check-bit-overhead]
---

# Slide 6

![Original slide 6](../../../public/generated/week-02-lecture-05/slide-006.png)

## Explanation

Different checks cover different portions of a packet. The IPv4 checksum is computed only over the IP header, while TCP’s checksum covers the TCP header and its payload. Therefore, an IP-header checksum cannot detect corruption that occurs only in the IP payload. [week-02-lecture-05, p. 6]

## Walkthrough

The slide highlights two design trade-offs when choosing an error-checking function:

- **Computation cost:** the sender and receiver must calculate the check efficiently.
- **Number of check bits:** extra check bits improve the amount of information available for detection, but they increase communication overhead.

So a practical protocol balances detection capability, processing time, and extra bytes transmitted. [week-02-lecture-05, p. 6]

## Connections and exam relevance

The scope matters. A check protects only the fields included in its calculation. This is why a payload may still have protection from TCP or another upper layer even when the IP header checksum does not cover that payload. [week-02-lecture-05, p. 6]

## Check your understanding

What portion does the IP checksum cover, and how is that different from the TCP checksum shown here?

Student response: The IP checksum covers only the IP header, while the TCP checksum covers the TCP header and payload.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-05, p. 6]
