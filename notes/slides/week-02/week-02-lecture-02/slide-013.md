---
slide_id: "week-02-lecture-02-slide-013"
source_id: "week-02-lecture-02"
page: 13
week: 2
status: understood
concepts: [heterogeneous-networks, ip-internetworking, router-layer-3-forwarding]
---

# Slide 13

![Original slide 13](../../../public/generated/week-02-lecture-02/slide-013.png)

## Explanation

This slide gives a concrete example of IP combining different network technologies. A can send data to B even though the path includes local networks, a fiber network, and another local network. IP provides the common network-layer service that connects these different link systems. [week-02-lecture-02, p. 13]

## Walkthrough

In the diagram, Host A first uses its local network and switch. The traffic then crosses a fiber network containing Layer 3 switches, which are routers. Finally, it reaches the local network and switch containing Host B. The lower-layer technology can change from one part of the path to another, but IP gives the routers a common way to forward packets toward B. [week-02-lecture-02, p. 13]

## Connections and exam relevance

Examples of lower-layer technologies include Ethernet, IEEE 802.11/Wi-Fi, SONET over optical fiber, and ATM. The application does not need separate application logic for each of these technologies; IP abstracts the differences and allows them to participate in one internetwork. This is the practical benefit of the hourglass architecture. [week-02-lecture-02, p. 13]

## Check your understanding

Why can Host A communicate with Host B even when the path between them uses different link technologies?

Student response: IP provides the common packet format and forwarding service; the lower layers can carry it using different frame formats and physical media.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 13]
