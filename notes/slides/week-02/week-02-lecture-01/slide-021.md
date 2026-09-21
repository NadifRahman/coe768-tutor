---
slide_id: "week-02-lecture-01-slide-021"
source_id: "week-02-lecture-01"
page: 21
week: 2
status: unseen
concepts: []
---

# Slide 21

![Original slide 21](../../../public/generated/week-02-lecture-01/slide-021.png)

## Explanation

This slide traces exactly what the parent and child do after `accept()` and `fork()`. The child handles the client; the parent remains the listener and immediately continues its accept loop [week-02-lecture-01, p. 21].

## Walkthrough

The sequence is:

1. Both processes begin with `new_sd` referring to the accepted client connection and `sd` referring to the listening socket.
2. In the child branch (`fork() == 0`), close `sd` and call `echod(new_sd)`. The child then exits when the client session ends.
3. In the parent branch (`fork() > 0`), close `new_sd` and loop back to `accept(sd, ...)`.

Closing the unused copy is important for clean resource management and correct connection lifetime. The parent does not handle the client’s data; the child does.

## Connections and exam relevance

This is the operational trace of the concurrent server and is a strong code-reading target: identify the process branch, the descriptor it closes, and the function that runs next [week-02-lecture-01, p. 21].

## Check your understanding

Which process calls `echod(new_sd)`, and what does the other process do immediately afterward?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 21]
