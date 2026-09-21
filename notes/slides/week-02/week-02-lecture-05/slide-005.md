---
slide_id: "week-02-lecture-05-slide-005"
source_id: "week-02-lecture-05"
page: 5
week: 2
status: understood
concepts: [checksum, ip-checksum, error-detection, end-to-end-check]
---

# Slide 5

![Original slide 5](../../../public/generated/week-02-lecture-05/slide-005.png)

## Explanation

A **checksum** is another error-detection method. The sender applies an algorithm to the data values, obtains a checksum, and appends it to the packet. The receiver applies the same algorithm to the received data and checks whether the result matches the transmitted checksum. [week-02-lecture-05, p. 5]

## Walkthrough

In the slide’s notation, the sender has data `C` and computes `s = g(C)`. It sends both the data and `s`. If the receiver gets altered data `C'`, it computes `g(C')` and compares it with the received `g(C)`:

- `g(C') = g(C)`: the check passes.
- `g(C') ≠ g(C)`: an error is detected.

The example shows a checksum associated with an IP packet. This illustrates that error checks can exist at more than one layer: the link layer may use an FCS for a local frame, while a network or transport protocol may use a checksum for its own packet or segment. [week-02-lecture-05, p. 5]

## Connections and exam relevance

The checksum is not the same thing as the packet data or the IP address. It is a compact summary calculated from the data. Because it is much shorter than the data, a matching checksum is strong evidence of correctness but not an absolute proof that no error occurred. [week-02-lecture-05, p. 5]

## Check your understanding

What does the receiver compare after recalculating the checksum?

Student response: The checksum is similar to the FCS, but they can operate at different layers and both can be present at the same time.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-05, p. 5]
