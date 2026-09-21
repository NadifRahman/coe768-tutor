---
slide_id: "week-02-lecture-01-slide-022"
source_id: "week-02-lecture-01"
page: 22
week: 2
status: unseen
concepts: []
---

# Slide 22

![Original slide 22](../../../public/generated/week-02-lecture-01/slide-022.png)

## Explanation

This diagram tracks the socket descriptors as a connection moves through the concurrent-server lifecycle. It shows why `sd` and `new_sd` have different roles before and after `accept()` and `fork()` [week-02-lecture-01, p. 22].

## Walkthrough

1. **Before `accept()` returns:** the server has `sd`, which is listening. The client’s `connect()` sends a request to it.
2. **After `accept()` returns:** the server still has listening `sd`, plus `new_sd`, which represents the client’s connected socket.
3. **After `fork()` returns:** both parent and child initially have copies of both descriptors.
4. **After the appropriate closes:** the parent keeps only `sd` and continues accepting; the child keeps only `new_sd` and handles the client.

The client remains connected to the child’s connected socket through the same TCP connection. The descriptor is a process-local handle, so the parent and child can each close their own copy without changing the other process’s descriptor table immediately.

## Connections and exam relevance

This is the visual summary of Slides 17, 19, and 21. Descriptor ownership across the four stages is a common code-tracing task: listening `sd` belongs to the parent, while connected `new_sd` belongs to the child after cleanup [week-02-lecture-01, p. 22].

## Check your understanding

After the parent and child close their unused descriptor copies, which process owns the listening socket and which process owns the connected socket?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 22]
