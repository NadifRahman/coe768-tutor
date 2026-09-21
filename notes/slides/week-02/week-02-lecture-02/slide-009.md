---
slide_id: "week-02-lecture-02-slide-009"
source_id: "week-02-lecture-02"
page: 9
week: 2
status: understood
concepts: [course-network-model, tcp-udp-ip-stack, protocol-layer-responsibilities]
---

# Slide 9

![Original slide 9](../../../public/generated/week-02-lecture-02/slide-009.png)

## Explanation

For this course, the practical stack emphasizes the layers and protocols used in Internet programming: Application, TCP/UDP transport, IP, a data-link layer, and the Physical layer. The slide reinforces what each level contributes: signals at Physical, local-link delivery at Data Link, multi-network packet delivery at IP, and end-to-end delivery through TCP or UDP. [week-02-lecture-02, p. 9]

## Walkthrough

Read the central stack from top to bottom:

- Application: labs and projects use application protocols and services.
- TCP/UDP: provides different kinds of end-to-end delivery.
- IP: sends packets across multiple networks.
- Second layer/Data Link: handles local Ethernet, Wi-Fi, or point-to-point links.
- Physical: sends bits as signals.

The slide also notes that presentation and session functions are often supplied by software libraries rather than appearing as separate protocol layers. [week-02-lecture-02, p. 9]

## Connections and exam relevance

This is the model we should use when analyzing the course's socket programs and network examples. When you see an application using TCP, the conceptual path is Application → TCP → IP → Data Link → Physical. With UDP, only the transport protocol changes; IP and the lower layers still carry the datagrams. [week-02-lecture-02, p. 9]

## Check your understanding

If a socket program uses UDP over Wi-Fi to contact a server on another network, which protocol belongs to each of the Application, Transport, Internet, and local-link portions of the stack?

Student response: The application uses its application protocol, UDP is the transport protocol, IP is the Internet-layer protocol, and Wi-Fi provides the local link and physical transmission.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 9]
