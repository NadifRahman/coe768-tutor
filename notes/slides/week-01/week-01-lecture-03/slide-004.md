---
slide_id: "week-01-lecture-03-slide-004"
source_id: "week-01-lecture-03"
page: 4
week: 1
status: understood
concepts: []
---

# Slide 4

![Original slide 4](../../../public/generated/week-01-lecture-03/slide-004.png)

## Explanation

This slide gives two request–reply examples: DNS for finding a destination address, and an echo service for demonstrating basic message exchange.

## Walkthrough

In the DNS example, the client first asks a DNS server for the IP address associated with a domain name. The DNS server returns the IP address. The client can then send an HTTP request to the web server at that address and receive an HTTP response containing the webpage. DNS and HTTP are separate application-level protocols and may involve different server processes.

The domain name remains useful to the application and user, while IP addressing is used for network delivery. Cloudflare is one possible DNS provider, but DNS is a distributed system with many providers and servers.

In the echo example, Client 1 sends “Hello” and the server sends “Hello” back. Client 2 sends “My name is Jason,” and the server echoes that message back to Client 2. The key behavior is that the server returns the received message to the client that sent it. A server can communicate with multiple clients, keeping each exchange associated with the correct client.

## Connections and exam relevance

These examples connect the client/server architecture to real application protocols and to the socket API: DNS, HTTP, and echo services all use request–reply communication, but each defines its own message meanings and behavior. [week-01-lecture-03, p. 4]

## Check your understanding

**Check:** Why does a browser typically contact a DNS server before sending an HTTP request to a web server?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 4]
