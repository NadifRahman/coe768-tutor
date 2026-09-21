---
slide_id: "week-02-lecture-01-slide-007"
source_id: "week-02-lecture-01"
page: 7
week: 2
status: unseen
concepts: []
---

# Slide 7

![Original slide 7](../../../public/generated/week-02-lecture-01/slide-007.png)

## Explanation

`listen()` changes a bound TCP socket from an ordinary, unconnected socket into a **passive listening socket**. It tells the operating system to accept incoming connection requests addressed to that socket. It does not itself complete a client connection or exchange application data [week-02-lecture-01, p. 7].

## Walkthrough

```c
int listen(int sockfd, int backlog);
```

` sockfd` is the descriptor created by `socket()` and usually assigned an address with `bind()`. `backlog` controls how many incoming connection requests the kernel should queue while the server is busy or before the server calls `accept()`.

For example, `listen(sd, 5)` asks for a queue capacity of five pending connections. If the queue fills, additional connection attempts may be rejected or otherwise delayed according to the system's behavior. The server's expected load should guide the value. A successful call returns `0`; an error returns `-1`.

## Connections and exam relevance

The server sequence is now `socket()` → `bind()` → `listen()` → `accept()`. The distinction between a listening socket and a connected socket is central: `listen()` prepares the former, while `accept()` obtains the latter. An assessment could test the ordering or the purpose of `backlog` [week-02-lecture-01, p. 7].

## Check your understanding

If a server has called `listen()` but has not yet called `accept()`, what is the kernel doing with a new client's connection request?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 7]
