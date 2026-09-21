---
slide_id: "week-02-lecture-02-slide-012"
source_id: "week-02-lecture-02"
page: 12
week: 2
status: understood
concepts: [internet-hourglass, ip-narrow-waist, heterogenous-network-interconnection]
---

# Slide 12

![Original slide 12](../../../public/generated/week-02-lecture-02/slide-012.png)

## Explanation

The hourglass architecture explains why the Internet can support many kinds of applications and physical networks. IP forms the narrow “waist”: it provides the minimal common network-layer functionality needed for global interconnectivity. Many protocols and applications can exist above IP, and many different link and physical technologies can exist below it. [week-02-lecture-02, p. 12]

## Walkthrough

From top to bottom, the diagram shows applications such as email, the Web, and phone services; application protocols such as SMTP, HTTP, and RTP; transport protocols such as TCP and UDP; IP; link protocols such as Ethernet and PPP; and physical media such as copper, fiber, and radio.

The narrow waist is powerful because every upper-layer protocol only needs to use IP to reach other networks, and IP can run over many different lower-layer technologies. A Web application does not need to know whether a packet ultimately travels over copper, fiber, Wi-Fi, or another link technology. [week-02-lecture-02, p. 12]

## Connections and exam relevance

This is a concrete example of layering, abstraction, and reuse. IP hides the details of the underlying network technology from applications, while giving lower layers a common service to carry many kinds of traffic. It also explains why replacing a local link technology does not require rewriting HTTP or TCP. [week-02-lecture-02, p. 12]

## Check your understanding

Why is IP called the “narrow waist” of the Internet hourglass, and what two kinds of diversity does it allow above and below itself?

Student response: IP is the common minimal layer that supports many upper-layer applications and protocols while running over many different lower-layer link and physical technologies.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 12]
