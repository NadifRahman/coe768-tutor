---
slide_id: "week-02-lecture-01-slide-014"
source_id: "week-02-lecture-01"
page: 14
week: 2
status: unseen
concepts: []
---

# Slide 14

![Original slide 14](../../../public/generated/week-02-lecture-01/slide-014.png)

## Explanation

This slide gives the tradeoff for iterative servers. They are simple and work well when each transaction is short. When processing takes longer, clients accumulate in the waiting queue and response time grows [week-02-lecture-01, p. 14].

## Walkthrough

Client A reaches the iterative server first and occupies its application logic. Client B may also send a request toward the server, but the server cannot process B until A's transaction finishes and its connected socket is closed. The diagram's two arrows show demand from both clients; the single server box represents the single serial worker.

This is not necessarily a failure of TCP. TCP can queue connection requests, but the application architecture chooses to serve them one at a time.

## Connections and exam relevance

This motivates the next design choice: concurrent servers, which arrange for multiple client transactions to make progress at the same time. An assessment may ask you to reason about queue growth and latency as transaction duration increases [week-02-lecture-01, p. 14].

## Check your understanding

Why is an iterative server acceptable for short transactions but problematic for long ones?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 14]
