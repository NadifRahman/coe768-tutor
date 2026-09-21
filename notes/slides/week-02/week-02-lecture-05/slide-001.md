---
slide_id: "week-02-lecture-05-slide-001"
source_id: "week-02-lecture-05"
page: 1
week: 2
status: understood
concepts: [noise, bit-error, error-detection, error-coding]
---

# Slide 1

![Original slide 1](../../../public/generated/week-02-lecture-05/slide-001.png)

## Explanation

The physical layer can alter transmitted bits because of noise. Error coding adds structured redundancy to the data so the receiver can determine whether the received bits are consistent with what was sent. The link layer uses this information to detect errors before passing a corrupted frame upward. [week-02-lecture-05, p. 1]

## Walkthrough

The diagram separates four ideas:

- **Transmitted data:** the intended bit sequence, shown as `0 1 0 0 1 0`.
- **Transmitted signal:** the physical waveform representing those bits.
- **Noise:** unwanted random energy added by the physical medium.
- **Received signal/data:** the receiver observes the combined signal and may decode one bit incorrectly. In the figure, one intended `0` is decoded as `1`, producing a bit error.

The key point is that the receiver cannot simply assume every received bit is correct. Error coding gives the receiver a test for detecting that corruption. [week-02-lecture-05, p. 1]

## Connections and exam relevance

This is why the link layer needs an error-detection field in its frame. It usually detects a damaged frame and discards it or triggers a local recovery mechanism; it does not make the physical channel perfectly noise-free. [week-02-lecture-05, p. 1]

## Check your understanding

If noise changes one transmitted bit, what problem does error coding help the receiver identify?

Student response: Error coding helps identify that noise corrupted the received data.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-05, p. 1]
