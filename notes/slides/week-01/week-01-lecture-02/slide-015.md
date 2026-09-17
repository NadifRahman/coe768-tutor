---
slide_id: "week-01-lecture-02-slide-015"
source_id: "week-01-lecture-02"
page: 15
week: 1
status: teaching
concepts: []
---

# Slide 15

![Original slide 15](../../../public/generated/week-01-lecture-02/slide-015.png)

## Explanation

The **network cloud** is an abstraction: an application uses the network’s communication service without needing to know every internal device or route.

## Walkthrough

The diagram shows applications on one host sending data through the cloud to applications on another host. The cloud hides the internal switches, routers, links, and provider networks. This does not mean those components are unimportant; it means the application can rely on the network’s interface and focus on its own task.

For example, an email or chat application needs to send data to a remote application. It does not normally select each router itself. It asks the operating system and networking stack to send the data, and the network handles forwarding. **Outside enrichment:** in practical programming, applications commonly access this service through an API such as a socket interface.

## Connections and exam relevance

This abstraction connects the component model to application programming: hosts and applications are endpoints, while the network cloud provides communication between them. It also prepares for the question of how applications interact with the network without directly controlling its internal hardware. [week-01-lecture-02, p. 15]

## Check your understanding

**Check:** Why can an application usually treat the network as a cloud instead of knowing the details of every router and link inside it?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-02, p. 15]
