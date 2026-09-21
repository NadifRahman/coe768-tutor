---
slide_id: "week-02-lecture-02-slide-015"
source_id: "week-02-lecture-02"
page: 15
week: 2
status: understood
concepts: [ip-interoperability, modular-evolution, internet-innovation]
---

# Slide 15

![Original slide 15](../../../public/generated/week-02-lecture-02/slide-015.png)

## Explanation

This slide emphasizes the architectural benefit of placing IP in the middle. IP allows different link-layer and physical technologies below it to interoperate, while allowing many applications and transport protocols above it. Because they share IP as a common layer, technologies above and below IP can evolve independently. [week-02-lecture-02, p. 15]

## Walkthrough

Imagine replacing Ethernet with a new link technology. If that technology can carry IP packets, applications such as HTTP and transport protocols such as TCP or UDP can continue to work without being redesigned. Likewise, a new application can use the existing IP and link-layer infrastructure. This is why the slide describes IP as connecting diversity below with diversity above. [week-02-lecture-02, p. 15]

## Connections and exam relevance

This is layering as a form of modularity: each layer exposes a common service upward and hides implementation details below. IP provides interoperability across different networks and physical media, which supports the Internet's ability to grow and incorporate new technologies. [week-02-lecture-02, p. 15]

## Check your understanding

If a new link technology can carry IP packets, why can existing applications such as HTTP continue to use it without being rewritten?

Student response: Higher layers only depend on IP's interface contract, so they do not need to know how the lower layer is implemented.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 15]
