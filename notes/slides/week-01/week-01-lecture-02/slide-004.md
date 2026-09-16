---
slide_id: "week-01-lecture-02-slide-004"
source_id: "week-01-lecture-02"
page: 4
week: 1
status: review-needed
concepts: []
---

# Slide 4

![Original slide 4](../../../public/generated/week-01-lecture-02/slide-004.png)

## Explanation

Wireless links have two important properties highlighted here: their transmissions are broadcast over the surrounding area, and the medium is half duplex.

## Walkthrough

**Broadcasting** means a transmitted message is available to all nodes within the wireless coverage area, rather than travelling only along one private physical wire. The dotted circle represents the access point’s coverage region. Devices inside it may receive the transmission. A device outside the region may detect a weak signal but still be unable to decode the message correctly.

More precisely, the radio wave can still reach the outside computer, but the signal may be too weak relative to noise. Decoding requires distinguishing the transmitted 1s and 0s; when the signal fades, those decisions become unreliable, so error checks may fail and the packet cannot be reconstructed correctly.

Wireless is **half duplex** on the same frequency: a device cannot send and receive in both directions at the same time on that shared channel. Devices therefore take turns, which is why wireless networks need coordination mechanisms such as CSMA/CA.

## Connections and exam relevance

This slide connects link directionality to wireless behavior and reinforces the earlier distinction between receiving a signal and successfully interpreting its data. It also explains why broadcast wireless media require careful resource allocation. [week-01-lecture-02, p. 4]

## Check your understanding

**Check:** Why might a computer outside the dotted coverage area detect an access-point signal but still be unable to decode the message correctly?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 4]
