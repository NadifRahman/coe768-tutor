---
slide_id: "week-01-lecture-03-slide-012"
source_id: "week-01-lecture-03"
page: 12
week: 1
status: teaching
concepts:
  - tcp-versus-udp
---

# Slide 12

![Original slide 12](../../../public/generated/week-01-lecture-03/slide-012.png)

## Explanation

TCP is connection-oriented: the communicating devices establish a connection before sending data and close it afterward. TCP provides reliable delivery, so it uses additional control and recovery mechanisms.

UDP is connectionless: it avoids the overhead of establishing, maintaining, and terminating a connection. This makes it efficient, but delivery is not guaranteed.

## Walkthrough

The slide groups common applications by transport protocol:

- TCP: HTTP, HTTPS, FTP, SMTP, and Telnet.
- UDP: DNS, DHCP, SNMP, and VoIP.

The choice depends on the application's needs. A web page or file transfer usually benefits from reliable delivery. A DNS lookup or voice call may prefer low overhead and can tolerate some loss or handle it at the application level.

### Clarification: why DNS commonly uses UDP

DNS does not simply accept losing the answer. A normal DNS query is small and usually fits in one datagram, so UDP avoids TCP connection setup and is efficient for the many short queries made by clients. If the query or response is lost, the resolver can wait, retry, use another DNS server, or use a cached answer. DNS can also fall back to TCP when a response is too large or when reliability is required, such as for zone transfers. Modern DNS variants such as DNS over TLS and DNS over HTTPS use stream-based transports.

Real-world examples:

- HTTP: loading a website or calling a web API. HTTPS is HTTP protected by TLS.
- FTP: transferring files to or from a server, historically common for hosting and enterprise file exchange. SFTP is a different protocol that runs over SSH.
- Telnet: an old remote command-line login protocol; it is insecure and is mostly replaced by SSH, though Telnet can still be used for simple device testing.
- DNS: turning `example.com` into an IP address when a browser or app needs to contact the service.
- DHCP: automatically giving a device an IP address, gateway, and DNS server when it joins a home Wi-Fi network.

## Connections and exam relevance

The previous slides introduced TCP's handshake and termination and UDP's lack of connection establishment. This slide summarizes the central trade-off: TCP offers reliability with more overhead; UDP offers efficiency without guaranteed delivery.

## Check your understanding

Why might a voice call use UDP while a file transfer uses TCP?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 12]
