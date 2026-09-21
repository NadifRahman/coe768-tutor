---
slide_id: "week-02-lecture-01-slide-025"
source_id: "week-02-lecture-01"
page: 25
week: 2
status: unseen
concepts: []
---

# Slide 25

![Original slide 25](../../../public/generated/week-02-lecture-01/slide-025.png)

## Explanation

This diagram shows the standard UDP client/server call sequence. The server binds a socket, receives datagrams, and sends replies. The client sends a datagram, receives a reply, and closes its socket when finished [week-02-lecture-01, p. 25].

## Walkthrough

### UDP server

    socket() -> bind() -> recvfrom() -> sendto() -> recvfrom() -> ...

recvfrom() receives one datagram and also provides the sender's address. The server uses that address in sendto() to return the response to the correct client. It can repeat this loop for different clients with the same socket.

### UDP client

    socket() -> sendto() -> recvfrom() -> close()

The client gives sendto() the server's destination address. It then calls recvfrom() for the reply. There is no connect() handshake, and the server never calls accept().

## Connections and exam relevance

This is the operational counterpart to the conceptual UDP model in Slide 24 and contrasts directly with the TCP sequence. An assessment may ask you to replace TCP calls with the correct UDP calls or identify where the peer address is supplied [week-02-lecture-01, p. 25].

## Check your understanding

Which call gives the UDP server the client’s address, and which call uses that address to send the reply?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 25]
