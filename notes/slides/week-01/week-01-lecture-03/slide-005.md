---
slide_id: "week-01-lecture-03-slide-005"
source_id: "week-01-lecture-03"
page: 5
week: 1
status: teaching
concepts: []
---

# Slide 5

![Original slide 5](../../../public/generated/week-01-lecture-03/slide-005.png)

## Explanation

The socket API can expose different transport services to applications. This slide introduces TCP and UDP as two choices.

## Walkthrough

**TCP** provides reliable application-data delivery between the two applications. It is responsible for ensuring that data is delivered appropriately, including handling problems such as loss or reordering through transport mechanisms.

**UDP** provides a simpler, best-effort way to send application data. It does not provide the same reliability guarantees; an application may need to tolerate loss or implement its own recovery if required.

The diagrams show the application using the socket API, the socket API handing data to the selected transport service, and matching TCP-to-TCP or UDP-to-UDP communication at the remote host. The application chooses the service based on what its task needs.

## Connections and exam relevance

This connects the socket API to the transport layer and revisits the reliability problem from Lecture 1. TCP is appropriate when correct, complete delivery matters; UDP is useful when an application prefers a lightweight best-effort service or can handle loss itself. [week-01-lecture-03, p. 5]

## Check your understanding

**Check:** What is the central reliability difference between TCP and UDP from an application’s point of view?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 5]
