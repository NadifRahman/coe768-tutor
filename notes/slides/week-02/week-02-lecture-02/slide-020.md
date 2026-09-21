---
slide_id: "week-02-lecture-02-slide-020"
source_id: "week-02-lecture-02"
page: 20
week: 2
status: understood
concepts: [multiple-network-interfaces, mac-per-nic, ip-per-interface]
---

# Slide 20

![Original slide 20](../../../public/generated/week-02-lecture-02/slide-020.png)

## Explanation

Each Network Interface Controller (NIC) has its own MAC address. Therefore, a device with separate Ethernet and Wi-Fi interfaces normally has at least two MAC addresses—one for each interface. [week-02-lecture-02, p. 20]

## Walkthrough

For example, a laptop may have:

- One MAC address for its Ethernet adapter
- One MAC address for its Wi-Fi adapter

IP addressing follows the interface model as well: each interface can be assigned its own IP address appropriate to the network it is connected to. The device as a whole can therefore be reachable through different IP addresses depending on which interface and network are used. [week-02-lecture-02, p. 20]

## Connections and exam relevance

Do not confuse “the device” with “the interface.” MAC addresses identify local-link interfaces, and IP addresses are also normally configured on interfaces. A hostname or service name may resolve to multiple IP addresses, but that is a naming/selection mechanism rather than one IP literally representing two interfaces simultaneously. [week-02-lecture-02, p. 20]

## Check your understanding

If a laptop is connected to Wi-Fi and Ethernet at the same time, should you expect one MAC address or two? What about its IP addresses?

Student response: It normally has two MAC addresses and two IP addresses, one pair associated with each network interface.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 20]
