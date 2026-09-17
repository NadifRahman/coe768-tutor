---
slide_id: "week-01-lecture-03-slide-006"
source_id: "week-01-lecture-03"
page: 6
week: 1
status: teaching
concepts: []
---

# Slide 6

![Original slide 6](../../../public/generated/week-01-lecture-03/slide-006.png)

## Explanation

One host can run many network applications at the same time, so it may have multiple sockets. A **port number** helps distinguish those application endpoints on the same host.

## Walkthrough

In the diagram, the client host has separate sockets for HTTP, email, and FTP, and the server host has separate sockets for its corresponding services. The socket API connects each application to the appropriate transport service, shown here with TCP.

A port number is a logical addressing value. An IP address identifies a host; the port identifies the application endpoint on that host. In a real TCP exchange, the communication is distinguished by the combination of source IP, source port, destination IP, and destination port. The slide simplifies this to show that different applications need different port endpoints.

## Connections and exam relevance

Ports extend IP addressing from “which host?” to “which application on that host?” They are essential when one computer simultaneously runs a web service, email service, and FTP service. [week-01-lecture-03, p. 6]

## Check your understanding

**Check:** What does an IP address identify, and what does a port number identify?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 6]
