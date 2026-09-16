---
slide_id: "week-01-lecture-02-slide-007"
source_id: "week-01-lecture-02"
page: 7
week: 1
status: teaching
concepts: []
---

# Slide 7

![Original slide 7](../../../public/generated/week-01-lecture-02/slide-007.png)

## Explanation

Protocols use well-defined message formats, and each message has a precise meaning intended to trigger a predictable response.

## Walkthrough

The slide uses HTTP, the protocol used for web requests and responses. The browser sends a request such as `GET index.html`, identifies the HTTP version, and indicates the host it wants to contact. This is Message 1: browser to server.

The server then sends Message 2, a response. `HTTP/1.1 200 OK` indicates that the request succeeded and the webpage can be returned. `HTTP/1.1 404 Not Found` indicates that the requested resource could not be found. The exact format lets the browser interpret the server’s response correctly.

## Connections and exam relevance

This is a concrete example of the protocol definition from Slide 6: HTTP specifies message structure, exchange order, and response actions. It also makes the client/server interaction from Lecture 1 observable as a request followed by a response. [week-01-lecture-02, p. 7]

## Check your understanding

**Check:** What does the `200 OK` response tell the browser, and how does it differ from `404 Not Found`?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 7]
