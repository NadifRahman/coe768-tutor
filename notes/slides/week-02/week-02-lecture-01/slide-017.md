---
slide_id: "week-02-lecture-01-slide-017"
source_id: "week-02-lecture-01"
page: 17
week: 2
status: unseen
concepts: []
---

# Slide 17

![Original slide 17](../../../public/generated/week-02-lecture-01/slide-017.png)

## Explanation

This is the concurrent-server loop implemented with `fork()`. The server listens once, repeatedly accepts clients, and creates a child process to handle each connected client [week-02-lecture-01, p. 17].

## Walkthrough

The control flow is:

```c
listen(sd, 5);
while (1) {
    new_sd = accept(sd, ...);
    switch (fork()) {
    case 0:       /* child */
        close(sd);
        exit(echod(new_sd));
    default:      /* parent */
        close(new_sd);
        break;
    case -1:      /* error */
        /* report fork failure */
    }
}
```

After `fork()`, both processes initially inherit descriptors. The child closes the listening descriptor because it only needs to serve the accepted client. The parent closes its copy of `new_sd` because it only needs to keep listening. The child calls `echod(new_sd)` and exits when that client's work is complete; the parent loops back to `accept()`.

The return value of `fork()` identifies the process: `0` in the child, a positive child process ID in the parent, and `-1` on failure.

## Connections and exam relevance

This code directly implements the concurrent design from Slide 15 and reinforces why the listening and connected descriptors must be separated. An assessment may test the `fork()` return cases or ask which descriptor each process closes [week-02-lecture-01, p. 17].

## Check your understanding

Why does the child close `sd`, while the parent closes `new_sd`?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 17]
