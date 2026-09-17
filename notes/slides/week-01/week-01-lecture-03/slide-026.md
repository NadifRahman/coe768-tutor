---
slide_id: "week-01-lecture-03-slide-026"
source_id: "week-01-lecture-03"
page: 26
week: 1
status: teaching
concepts:
  - tcp-header-and-decapsulation
---

# Slide 26

![Original slide 26](../../../public/generated/week-01-lecture-03/slide-026.png)

## Explanation

This slide zooms in on decapsulation and a TCP header. The receiver processes the TCP header, uses its control fields, and removes that header before passing the application data upward.

## Walkthrough

The TCP header includes fields such as:

- Source and destination ports, identifying the applications at each endpoint.
- Sequence and acknowledgment numbers, supporting ordering and reliable delivery.
- Control flags, such as SYN, ACK, FIN, and RST, describing connection actions.
- Window size, supporting flow control.
- Checksum, supporting error detection.

The application data follows the TCP header. At the receiving host, TCP reads these fields, performs its transport-layer work, removes the header, and passes the remaining data to the correct application.

## Connections and exam relevance

This connects the abstract idea of encapsulation to the concrete information TCP adds. The TCP header is not application content; it is control information for TCP.

## Check your understanding

Name two pieces of information carried in a TCP header and explain what one of them is used for.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 26]
