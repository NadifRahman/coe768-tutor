---
slide_id: "week-02-lecture-04-slide-002"
source_id: "week-02-lecture-04"
page: 2
week: 2
status: understood
concepts: [link-layer-protocols, ethernet, wifi, ppp, hdlc]
---

# Slide 2

![Original slide 2](../../../public/generated/week-02-lecture-04/slide-002.png)

## Explanation

The data-link layer supports communication between nodes over a single network or link and commonly uses local-link addressing such as MAC addresses. Different physical and network environments use different data-link protocols. [week-02-lecture-04, p. 2]

## Walkthrough

Examples include:

- Ethernet for wired local networks
- IEEE 802.11 for Wi-Fi
- PPP for a direct point-to-point link, such as between two routers
- HDLC for certain satellite and ISDN links

Each protocol defines how data is framed and exchanged over its particular kind of link. [week-02-lecture-04, p. 2]

## Connections and exam relevance

The link-layer protocol is chosen for the current link, not necessarily for the entire end-to-end route. Ethernet may be used on one hop, Wi-Fi on another, and PPP or another protocol on a router-to-router link. A point-to-point protocol such as PPP may not need ordinary MAC addressing because there are only two endpoints; the broader principle is local-link delivery. [week-02-lecture-04, p. 2]

## Check your understanding

Why might the same end-to-end IP packet be carried by Ethernet on one link, Wi-Fi on another, and PPP between two routers?

Student response: The link-layer protocol can change per hop while IP provides the common end-to-end service.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-04, p. 2]
