---
slide_id: "week-01-lecture-03-slide-008"
source_id: "week-01-lecture-03"
page: 8
week: 1
status: teaching
concepts: []
---

# Slide 8

![Original slide 8](../../../public/generated/week-01-lecture-03/slide-008.png)

## Explanation

Port numbers are divided into ranges with different conventions for assigning services.

## Walkthrough

The slide focuses on two ranges:

- **0–1023:** well-known ports associated with standard services and commonly restricted to operating-system services, administrators, or privileged processes. Examples include FTP on 21, SSH on 22, SMTP on 25, and HTTP on 80.
- **1024–49151:** registered ports that applications can use without the same privileged-service restriction described for well-known ports.

The important idea is not that a port number automatically guarantees a service; rather, conventions make common services easier to identify. A program must actually be listening on a port for communication to succeed. The exact permission required to bind a port depends on the operating system and configuration.

Application example: an Nginx reverse proxy can listen publicly on port 80 or 443, accept browser requests, and forward them over a separate connection to a backend application listening on an internal port such as 3000 or 8080. The client still connects to the server’s public IP and port 80/443; Nginx then acts as a server toward the client and a client toward the backend. This is application-level proxying, distinct from simple NAT port forwarding.

## Connections and exam relevance

This extends the previous slide’s idea that ports identify services. Port conventions help clients know where to request HTTP, FTP, SSH, or email services, while the socket API uses the selected port when creating or connecting sockets. [week-01-lecture-03, p. 8]

## Check your understanding

**Check:** What is the difference between a well-known port and a registered port in the classification presented here?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 8]
