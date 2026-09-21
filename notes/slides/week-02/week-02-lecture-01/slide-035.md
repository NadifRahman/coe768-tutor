---
slide_id: "week-02-lecture-01-slide-035"
source_id: "week-02-lecture-01"
page: 35
week: 2
status: unseen
concepts: []
---

# Slide 35

![Original slide 35](../../../public/generated/week-02-lecture-01/slide-035.png)

## Explanation

This slide builds the UDP time server's address and socket. It chooses port 3000, accepts IPv4 traffic on any local interface, creates a datagram socket, and prepares to bind it [week-02-lecture-01, p. 35].

## Walkthrough

The address setup is:

    struct sockaddr_in sin;
    int port = 3000;
    sin.sin_family = AF_INET;
    sin.sin_addr.s_addr = INADDR_ANY;
    sin.sin_port = htons(port);

sin_family selects IPv4. INADDR_ANY means any local interface. htons() converts the host-order port number into network byte order; port fields in network structures must use this representation.

The socket is created with:

    s = socket(AF_INET, SOCK_DGRAM, 0);

The SOCK_DGRAM choice selects UDP. The negative return check detects socket-creation failure before the program attempts to bind.

## Connections and exam relevance

This is a more complete UDP version of the server setup from Slide 30 and introduces htons(). An assessment may test address-family selection, INADDR_ANY, network byte order, or the difference between SOCK_DGRAM and SOCK_STREAM [week-02-lecture-01, p. 35].

## Check your understanding

Why is the port passed through htons() before it is stored in sin.sin_port?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 35]
