---
slide_id: "week-02-lecture-01-slide-019"
source_id: "week-02-lecture-01"
page: 19
week: 2
status: unseen
concepts: []
---

# Slide 19

![Original slide 19](../../../public/generated/week-02-lecture-01/slide-019.png)

## Explanation

This slide restates the two mechanisms that make the concurrent server work: `accept()` creates a new connected descriptor, and `fork()` creates a new process that can handle it [week-02-lecture-01, p. 19].

## Walkthrough

After `accept()`:

- the returned descriptor represents the new client connection;
- the original socket remains open, unconnected, and listening.

The Unix declaration is:

```c
#include <unistd.h>
pid_t fork(void);
```

`fork()` is called once in the source code but returns in two processes:

- parent: receives the new child’s process ID;
- child: receives `0`.

This is why a `switch(fork())` can direct the child and parent into different code paths.

## Connections and exam relevance

This provides the formal explanation behind the descriptor-closing pattern on Slide 17. Be able to distinguish “new socket” from “new process” and understand that `fork()` creates the process while `accept()` creates the connected socket [week-02-lecture-01, p. 19].

## Check your understanding

Which function creates the connected socket, and which function creates the child process?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 19]
