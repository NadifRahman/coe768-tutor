---
slide_id: "week-01-lecture-03-slide-011"
source_id: "week-01-lecture-03"
page: 11
week: 1
status: teaching
concepts:
  - udp-connectionless-and-error-detection
---

# Slide 11

![Original slide 11](../../../public/generated/week-01-lecture-03/slide-011.png)

## Explanation

UDP is connectionless: an application can hand a datagram to UDP without first completing a TCP-style handshake. UDP still uses IP addresses and port numbers so the datagram can reach the intended host and application.

UDP can detect that a datagram was corrupted, but it does not provide built-in recovery such as retransmission or ordering guarantees. If a datagram is lost or fails its integrity check, recovery is left to the application.

## Walkthrough

1. An application gives data to UDP.
2. UDP sends it through the network without connection-establishment messages.
3. The receiving host's UDP layer checks the datagram and, if valid, delivers it to the application selected by the destination port.
4. If it is missing or corrupted, UDP does not automatically request a replacement.

The one-way-looking diagram shows one datagram's path; UDP can send datagrams in both directions independently.

## Connections and exam relevance

This contrasts with TCP: TCP establishes a connection and provides reliable, ordered delivery, while UDP has lower setup overhead and leaves reliability needs to the application. “Connectionless” does not mean “addressless”—IP addresses and ports are still needed for delivery.

## Check your understanding

What does “connectionless” mean in UDP, and what happens if a UDP datagram is lost or corrupted?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 11]
