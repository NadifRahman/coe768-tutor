---
slide_id: "week-02-lecture-01-slide-015"
source_id: "week-02-lecture-01"
page: 15
week: 2
status: unseen
concepts: []
---

# Slide 15

![Original slide 15](../../../public/generated/week-02-lecture-01/slide-015.png)

## Explanation

A **concurrent server** allows multiple client transactions to make progress at the same time. After accepting Client A, the server creates a child server process dedicated to A. The main server can then continue accepting Client B instead of waiting for A to finish [week-02-lecture-01, p. 15].

## Walkthrough

The diagram shows two roles inside the server machine:

- The main/concurrent server keeps the listening socket and accepts new clients.
- A child server process handles the connected socket for one client.

The simplest technique presented here is Unix `fork()`: create one child process per client. The child performs the long transaction while the parent returns to its accept loop. Threads are another possible technique, but this course does not cover thread-based servers in this section.

The benefit is responsiveness for independent clients; the cost is the resources and coordination required for multiple processes.

## Connections and exam relevance

This is the solution to the queueing problem in Slides 13–14. Be able to identify which process owns the listening role, which process handles a client, and how `fork()` changes one serial server into multiple workers [week-02-lecture-01, p. 15].

## Check your understanding

After the parent server forks a child to handle Client A, what should the parent do so Client B can be served?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 15]
