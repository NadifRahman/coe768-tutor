---
slide_id: "week-02-lecture-02-slide-030"
source_id: "week-02-lecture-02"
page: 30
week: 2
status: understood
concepts: [local-versus-end-to-end-error-control, link-retransmission, tcp-reliability-scope]
---

# Slide 30

![Original slide 30](../../../public/generated/week-02-lecture-02/slide-030.png)

## Explanation

This slide contrasts the scope of error control at two layers. The data-link layer controls errors over one physical link between neighboring nodes. The transport layer controls errors over the entire end-to-end network connection between the source and destination systems. [week-02-lecture-02, p. 30]

## Walkthrough

Suppose a frame is corrupted on one local link. A data-link protocol may detect that local error and retransmit the frame across that link. But the transport layer still provides end-to-end protection because a packet could be lost or damaged elsewhere along the route. TCP at the endpoints can detect missing data and recover; link-layer recovery alone cannot guarantee that the complete message reached the destination. [week-02-lecture-02, p. 30]

## Connections and exam relevance

The same data can therefore receive protection at multiple scopes. Local link control can improve efficiency by repairing a nearby problem quickly, while transport control verifies the complete path. These mechanisms are complementary rather than duplicates with exactly the same responsibility. [week-02-lecture-02, p. 30]

## Check your understanding

If a frame is successfully delivered across one link but is later lost at another router, which layer can still detect the end-to-end loss?

Student response: The transport layer can detect the end-to-end loss.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 30]
