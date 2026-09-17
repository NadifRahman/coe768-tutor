---
slide_id: "week-01-lecture-03-slide-018"
source_id: "week-01-lecture-03"
page: 18
week: 1
status: teaching
concepts:
  - http-as-application-protocol
---

# Slide 18

![Original slide 18](../../../public/generated/week-01-lecture-03/slide-018.png)

## Explanation

Network functions and services are implemented through protocols. HTTP is an application-layer protocol that defines how a client requests web resources and how a server responds.

## Walkthrough

The example request is:

`GET index.html HTTP/1.1` with a `Host` such as `www.google.ca`.

The server responds with a status such as:

- `200 OK`: the requested resource was found and returned.
- `404 Not Found`: the server could not find the requested resource.

The exact HTTP version shown on the response is less important here than the request/response structure and the status code.

## Connections and exam relevance

This connects the general idea of protocols to a concrete application service: HTTP defines message format, request method, ordering of the exchange, and the action the server should take.

## Check your understanding

What does `200 OK` mean, and how is it different from `404 Not Found`?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 18]
