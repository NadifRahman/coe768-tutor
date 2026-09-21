---
slide_id: "week-02-lecture-01-slide-020"
source_id: "week-02-lecture-01"
page: 20
week: 2
status: unseen
concepts: []
---

# Slide 20

![Original slide 20](../../../public/generated/week-02-lecture-01/slide-020.png)

## Explanation

`fork()` returns twice because one call creates a second process. The parent and child both continue from the instruction immediately after `fork()`, but the operating system gives them different return values so the program can choose different behavior [week-02-lecture-01, p. 20].

## Walkthrough

Conceptually:

```c
pid_t result = fork();

if (result == 0) {
    /* running in the child */
} else if (result > 0) {
    /* running in the parent; result is the child PID */
} else {
    /* creation failed */
}
```

Before the call there is one execution path. After a successful call there are two processes at the same point in the program. They have separate execution state, although they initially inherit many resources, including open file descriptors. That inheritance is why both processes initially have access to the listening and connected sockets, and why each must close the descriptor it does not use.

## Connections and exam relevance

This explains the `switch(fork())` logic in the echo server. An assessment may ask how many processes exist after repeated forks, which branch runs in each process, or why inherited descriptors need explicit closing [week-02-lecture-01, p. 20].

## Check your understanding

After a successful `fork()`, does the child restart the program from `main()`, or continue from a specific point? Which point?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 20]
