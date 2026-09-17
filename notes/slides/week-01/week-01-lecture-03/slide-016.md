---
slide_id: "week-01-lecture-03-slide-016"
source_id: "week-01-lecture-03"
page: 16
week: 1
status: teaching
concepts:
  - network-layering-and-modularity
---

# Slide 16

![Original slide 16](../../../public/generated/week-01-lecture-03/slide-016.png)

## Explanation

Layering prevents every application or protocol from having to reimplement all networking technology. Applications can use common lower-layer services for addressing, transport, and transmission.

The slide illustrates this with application protocols: Telnet provides a remote command-line interface, FTP transfers computer files, and HTTP transfers web content such as text, images, audio, and video.

## Walkthrough

Without layering, Telnet, FTP, HTTP, and every future application would each need its own complete solutions for moving data across networks. With layering, these applications can share the same lower-layer mechanisms while specializing only in their own application-level behavior.

## Connections and exam relevance

This is the practical payoff of modularity: adding or changing an application protocol does not require rebuilding the underlying network technologies.

## Check your understanding

What would application protocols such as HTTP and FTP have to do repeatedly if networking were not layered?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 16]
