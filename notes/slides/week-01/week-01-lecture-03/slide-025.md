---
slide_id: "week-01-lecture-03-slide-025"
source_id: "week-01-lecture-03"
page: 25
week: 1
status: teaching
concepts:
  - encapsulation-and-decapsulation
---

# Slide 25

![Original slide 25](../../../public/generated/week-01-lecture-03/slide-025.png)

## Explanation

Encapsulation is how layers add their own control information to data as it moves down the sender's protocol stack. A lower layer wraps the higher-layer data and may add a header before it, a trailer after it, or both.

Decapsulation is the reverse process at the receiver: each layer reads and removes the information intended for it, then passes the remaining data upward.

## Walkthrough

For example, an HTTP message is passed to TCP. TCP adds its control information, and a lower link layer adds information needed for delivery across the local network. At the receiving host, the link layer processes its wrapper, TCP processes its information, and the original HTTP data reaches the application.

Information added before the data is called a **header**. Information added after the data is called a **trailer**. Trailers can contain error-detection or error-correction bits.

## Connections and exam relevance

Encapsulation explains how protocols at different layers cooperate without mixing their responsibilities: each layer adds and later removes its own control information.

## Check your understanding

What is the difference between encapsulation and decapsulation, and what is a header or trailer?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 25]
