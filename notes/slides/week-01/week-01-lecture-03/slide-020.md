---
slide_id: "week-01-lecture-03-slide-020"
source_id: "week-01-lecture-03"
page: 20
week: 1
status: teaching
concepts:
  - layered-http-and-tcp-interaction
---

# Slide 20

![Original slide 20](../../../public/generated/week-01-lecture-03/slide-020.png)

## Explanation

This slide shows HTTP and TCP working together in two layers on both the browser and the web server. HTTP handles the web request and response; TCP underneath establishes the connection and provides reliable delivery.

## Walkthrough

The sequence shown is:

1. TCP sends `SYN`.
2. The server replies `SYN-ACK`.
3. The browser sends `ACK`, completing the TCP handshake.
4. HTTP sends the web request.
5. TCP acknowledges the request.
6. HTTP sends the web response.
7. TCP acknowledges the response.

Messages 1, 2, 3, 5, and 7 are TCP messages. Messages 4 and 6 are HTTP messages. The browser's HTTP layer calls its TCP layer, and TCP communicates with the peer TCP layer; the server's TCP layer then delivers the data to its HTTP layer.

## Connections and exam relevance

This is layering in action: peer protocols communicate horizontally with their counterparts, while adjacent layers interact vertically on the same host. The application does not need to implement TCP's handshake or acknowledgments itself.

## Check your understanding

Which messages in the diagram belong to TCP, and which belong to HTTP?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 20]
