---
slide_id: "week-02-lecture-05-slide-004"
source_id: "week-02-lecture-05"
page: 4
week: 2
status: understood
concepts: [fcs-verification, checksum-function, frame-corruption]
---

# Slide 4

![Original slide 4](../../../public/generated/week-02-lecture-05/slide-004.png)

## Explanation

The sender computes the FCS from the original data and appends it to the frame. The receiver then computes the same function on the data it actually received and compares the new result with the FCS that arrived in the trailer. A mismatch indicates that the frame was changed during transmission. [week-02-lecture-05, p. 4]

## Walkthrough

The slide uses `D` for the sender’s data and `f(D)` for the FCS calculated from that data. The transmitted frame is:

`[H | D | f(D)]`

If noise changes the data in transit, the receiver sees `D'` instead of `D`. It calculates `f(D')` and compares it with the received `f(D)`:

- If `f(D') = f(D)`, the check passes.
- If `f(D') ≠ f(D)`, the receiver detects an error.

The prime symbol in `D'` means “the received version,” which may differ from the original. [week-02-lecture-05, p. 4]

## Connections and exam relevance

The receiver does not need to know which individual bit changed. It only needs the comparison to reveal that the frame is inconsistent. In practice, a matching FCS means the frame passed the chosen check; it is not an absolute mathematical guarantee that no error occurred. [week-02-lecture-05, p. 4]

## Check your understanding

If the receiver gets `D'` instead of `D`, which two values does it compare to detect corruption?

Student response: It compares the checksum calculated from the received data with the checksum that arrived with the packet.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-05, p. 4]
