---
slide_id: "week-02-lecture-02-slide-029"
source_id: "week-02-lecture-02"
page: 29
week: 2
status: understood
concepts: [end-to-end-transport-control, transport-flow-control, transport-error-control]
---

# Slide 29

![Original slide 29](../../../public/generated/week-02-lecture-02/slide-029.png)

## Explanation

The transport layer provides end-to-end error control and flow control between the two end systems. The red arrow in the diagram connects the transport layers of the endpoints, while the intermediate network mainly forwards packets and frames. [week-02-lecture-02, p. 29]

## Walkthrough

Flow control prevents the sender from overwhelming the receiver. Error control detects loss or corruption and can support recovery, depending on the transport protocol. These functions are coordinated by the transport protocols at the endpoints, such as TCP. Routers and switches along the path do not normally participate in the application's end-to-end TCP conversation. [week-02-lecture-02, p. 29]

## Connections and exam relevance

This explains the phrase **end-to-end**: transport control belongs to the source and destination processes, not to every intermediate device. The network may change frames at each hop, but the transport relationship remains between the two end systems. UDP provides a lighter transport service and does not provide TCP's full reliability and flow-control behavior. [week-02-lecture-02, p. 29]

## Check your understanding

Why is transport-layer flow and error control shown only between the two end systems rather than between every pair of routers along the path?

Student response: The lower layers do not provide the same message-level end-to-end control; they mainly move information along the path. Clarification: lower layers may provide local flow/error control, but transport control covers the complete source-to-destination path.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 29]
