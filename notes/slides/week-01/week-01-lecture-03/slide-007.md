---
slide_id: "week-01-lecture-03-slide-007"
source_id: "week-01-lecture-03"
page: 7
week: 1
status: teaching
concepts: []
---

# Slide 7

![Original slide 7](../../../public/generated/week-01-lecture-03/slide-007.png)

## Explanation

Ports let the networking system deliver incoming data to the correct service on a host.

## Walkthrough

The server at IP address `10.1.1.1` runs both a web server on port 80 and an FTP server on port 21. A client that sends to `10.1.1.1:80` is asking for the web service; a client that sends to `10.1.1.1:21` is asking for the FTP service. The IP address selects the host, and the port selects the service on that host.

The lower example shows that the same client can target the same server at port 21 instead of port 80, changing which server process receives the communication. In a complete connection, the client also has its own source port so replies can be delivered back to the correct client socket.

## Connections and exam relevance

This makes the addressing role of ports concrete and connects directly to the socket diagrams from Slide 6. Port numbers allow multiple services to coexist on one server IP address. [week-01-lecture-03, p. 7]

## Check your understanding

**Check:** If a client sends data to `10.1.1.1:80`, which service should receive it, and what does the `80` identify?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 7]
