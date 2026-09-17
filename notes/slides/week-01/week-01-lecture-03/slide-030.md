---
slide_id: "week-01-lecture-03-slide-030"
source_id: "week-01-lecture-03"
page: 30
week: 1
status: teaching
concepts:
  - link-layer-independence-and-ip
---

# Slide 30

![Original slide 30](../../../public/generated/week-01-lecture-03/slide-030.png)

## Explanation

The browser can use the same HTTP and TCP software whether the client connects through Wi-Fi or Ethernet. The link and physical layers can differ, while IP provides a common network-layer method for carrying data from the source IP to the destination IP.

## Walkthrough

In the example, the mobile client uses an IEEE 802.11 Wi-Fi link to reach the access point, while the web server uses Ethernet on the wired LAN. The access point bridges the wireless and wired portions. The IP packet can continue toward the server, but each link may use its own frame format and local addressing details.

## Connections and exam relevance

This demonstrates why layering is valuable: HTTP and TCP do not need separate versions for Wi-Fi and Ethernet. Only the lower link/physical implementation changes.

## Check your understanding

What can remain the same when a client switches from Ethernet to Wi-Fi, and which part of the stack changes?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 30]
