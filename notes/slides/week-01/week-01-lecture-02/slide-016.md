---
slide_id: "week-01-lecture-02-slide-016"
source_id: "week-01-lecture-02"
page: 16
week: 1
status: teaching
concepts: []
---

# Slide 16

![Original slide 16](../../../public/generated/week-01-lecture-02/slide-016.png)

## Explanation

A **socket API** is the network-application interface between an application and the networking system provided by the operating system.

## Walkthrough

The diagram shows an application on each host using a socket interface to reach the network cloud. The socket API provides communication functions or system calls that an application can call to communicate with another application on a different computer.

The abstraction hides internal network details from the application programmer. The programmer does not need to implement every route through the Internet or decide how the network recovers from every lost transmission. Instead, the program uses the socket interface to express operations such as creating an endpoint, connecting or accepting a connection, sending data, and receiving data. The exact functions depend on the programming environment; the slide’s central point is the interface boundary.

## Connections and exam relevance

This is the concrete answer to the question posed on Slide 15: an application interacts with the network cloud through a socket API. It connects application-layer behavior to the host, protocol, and network infrastructure concepts introduced throughout Week 1. [week-01-lecture-02, p. 16]

## Check your understanding

**Check:** What does the socket API allow an application to do, and what network details does it allow the programmer to ignore?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 16]
