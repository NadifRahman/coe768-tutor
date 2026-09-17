---
slide_id: "week-01-lecture-03-slide-001"
source_id: "week-01-lecture-03"
page: 1
week: 1
status: teaching
concepts: []
---

# Slide 1

![Original slide 1](../../../public/generated/week-01-lecture-03/slide-001.png)

## Explanation

This lecture revisits the **socket API**, the software interface that lets application programs communicate with one another through a network.

## Walkthrough

API means **Application Programming Interface**. It is a software intermediary: one application calls defined interface operations, the local host and networking stack carry the data through the network, and the remote application receives it through its own interface. The diagram shows two applications above separate hosts, with a network-application interface between each application and its host’s networking system.

The socket API hides internal routing and transmission details. The application communicates through the interface rather than directly controlling routers, links, or the entire packet-delivery process.

## Connections and exam relevance

This reinforces Lecture 2’s network-cloud abstraction and begins the practical socket-programming portion of Week 1. [week-01-lecture-03, p. 1]

This slide intentionally repeats the socket-API idea from Lecture 2 as a transition: the definition is not substantially new, but the lecture now uses it as the foundation for practical socket communication and code.

## Check your understanding

This is a lecture-opening concept slide. The main idea to retain is that sockets are the application’s interface to network communication.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 1]
