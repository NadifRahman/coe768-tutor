---
slide_id: "week-01-lecture-03-slide-029"
source_id: "week-01-lecture-03"
page: 29
week: 1
status: teaching
concepts:
  - http-data-encapsulation
---

# Slide 29

![Original slide 29](../../../public/generated/week-01-lecture-03/slide-029.png)

## Explanation

This slide shows the later stage, after TCP has been established: HTTP application data is now being sent. Unlike the handshake messages, the TCP segment contains both a TCP header and an HTTP payload.

## Walkthrough

At the browser:

1. HTTP creates the request or receives application data from the browser.
2. TCP adds its header around that HTTP data.
3. Ethernet adds its local-link header and trailer around the TCP segment.
4. The resulting frame crosses the network.

At the server, the process reverses: Ethernet removes its wrapper, TCP processes and removes its header, and the HTTP data is delivered to the server application. The same process occurs in reverse for the HTTP response.

## Connections and exam relevance

This complements the previous slide: TCP handshake messages carried only TCP control information, while HTTP messages 4 and 6 carry application data inside TCP and Ethernet wrappers.

## Check your understanding

What new content appears inside the TCP segment when the HTTP request is sent?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 29]
