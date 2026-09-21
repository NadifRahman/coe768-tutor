---
slide_id: "week-02-lecture-01-slide-018"
source_id: "week-02-lecture-01"
page: 18
week: 2
status: unseen
concepts: []
---

# Slide 18

![Original slide 18](../../../public/generated/week-02-lecture-01/slide-018.png)

## Explanation

This diagram shows how one server port can support multiple simultaneous TCP connections. The parent `echo_server` keeps the listening socket `sd` on port `10000`; each accepted client gets a separate connected descriptor and child process, such as `new_sd1`/Child1 and `new_sd2`/Child2 [week-02-lecture-01, p. 18].

## Walkthrough

Client 1 uses `20.1.1.1:20011` and Client 2 uses `20.1.1.1:10011`. Both connect to the server at `10.1.1.1:10000`, but they are still distinct TCP connections because their client-side ports differ.

Conceptually, TCP identifies a connection using the four-tuple:

```text
(source IP, source port, destination IP, destination port)
```

So the two flows are:

```text
(20.1.1.1, 20011, 10.1.1.1, 10000)
(20.1.1.1, 10011, 10.1.1.1, 10000)
```

The shared destination port identifies the service; the different source ports let the operating system deliver each packet to the correct connected socket and child process.

## Connections and exam relevance

This explains how concurrency coexists with a single well-known server port and connects to the earlier discussion of ephemeral client ports. An assessment may ask you to distinguish connections by their four-tuples or identify which child process receives a packet [week-02-lecture-01, p. 18].

## Check your understanding

Why can Client 1 and Client 2 both connect to server port `10000` without their packets being confused?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 18]
