---
slide_id: "week-01-lecture-03-slide-003"
source_id: "week-01-lecture-03"
page: 3
week: 1
status: teaching
concepts: []
---

# Slide 3

![Original slide 3](../../../public/generated/week-01-lecture-03/slide-003.png)

## Explanation

This slide shows the basic request–reply interaction between a client process and a server process.

## Walkthrough

The client process runs on the client machine and sends a **request** through the network. The server process runs on the server machine, receives the request, performs the requested service, and sends a **reply** back through the network. The client then waits for that reply before continuing with the next step.

The example is a browser requesting a webpage. The browser is the client process, the web server is the server process, and the network cloud carries the two messages in opposite directions. The machines provide the computing environments; the processes are the specific programs participating in this exchange.

## Connections and exam relevance

This is the operational sequence behind the client/server architecture and HTTP example: request first, server processing, reply second. It is also the interaction that socket programs implement. [week-01-lecture-03, p. 3]

## Check your understanding

**Check:** What are the two messages exchanged in this example, and which process sends each one?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 3]
