---
slide_id: "week-02-lecture-02-slide-025"
source_id: "week-02-lecture-02"
page: 25
week: 2
status: understood
concepts: [network-layer-devices, layer-3-switch, virtual-versus-actual-communication]
---

# Slide 25

![Original slide 25](../../../public/generated/week-02-lecture-02/slide-025.png)

## Explanation

Network-layer devices perform data forwarding between end systems by routing and switching network-layer PDUs. A router, or Layer 3 switch, operates at the network layer and can connect different networks and technologies, such as 802.11/Wi-Fi and Ethernet. [week-02-lecture-02, p. 25]

## Walkthrough

The diagram distinguishes virtual communication from actual communication. The dotted line between network layers represents the logical end-to-end relationship for the network-layer PDU. The actual data path moves through each router's physical and data-link layers at every hop, then rises to the network layer again before continuing. [week-02-lecture-02, p. 25]

## Connections and exam relevance

This is the network-layer counterpart to the earlier switch diagram. A Layer 2 switch forwards local frames using MAC addresses. A router/Layer 3 switch forwards packets using IP information and can join separate networks, even when their link technologies differ. [week-02-lecture-02, p. 25]

## Check your understanding

What is the key difference between a Layer 2 switch and a Layer 3 switch/router in terms of what each forwards and which address it uses?

Student response: A Layer 2 switch forwards local frames using MAC addresses, while a Layer 3 switch/router forwards packets between networks using IP information.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 25]
