---
slide_id: "week-02-lecture-01-slide-030"
source_id: "week-02-lecture-01"
page: 30
week: 2
status: unseen
concepts: []
---

# Slide 30

![Original slide 30](../../../public/generated/week-02-lecture-01/slide-030.png)

## Explanation

This is the UDP echo server corresponding to the client on Slide 29. It creates a datagram socket, binds it to the server address and port, then repeatedly receives a datagram and sends the same payload back to the recorded client address [week-02-lecture-01, p. 30].

## Walkthrough

The setup is:

    sockfd = socket(AF_INET, SOCK_DGRAM, 0);
    bind(sockfd, &serveraddr, sizeof(serveraddr));

The main loop then does:

    n = recvfrom(sockfd, buf, BUFSIZE, 0,
                 &clientaddr, &clientlen);
    n = sendto(sockfd, buf, ..., 0,
               &clientaddr, clientlen);

The first call both receives the datagram and fills in clientaddr. The second call reuses that address as the destination, so the reply goes to the client that sent the message. The same server socket can repeat this for Client 1, Client 2, and so on; there is no per-client connected descriptor.

The example treats the payload as text with strlen(buf). A production implementation should track the byte count returned by recvfrom() so it can correctly echo binary data or text containing embedded null bytes.

## Connections and exam relevance

This is the complete UDP server implementation and contrasts with the TCP echo server: no listen(), accept(), fork(), or child process is required for the basic datagram loop [week-02-lecture-01, p. 30].

## Check your understanding

Why does the UDP server send its reply to clientaddr instead of to a permanently connected socket?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 30]
