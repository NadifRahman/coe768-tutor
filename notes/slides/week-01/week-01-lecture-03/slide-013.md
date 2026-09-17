---
slide_id: "week-01-lecture-03-slide-013"
source_id: "week-01-lecture-03"
page: 13
week: 1
status: teaching
concepts:
  - network-layering-and-modularity
---

# Slide 13

![Original slide 13](../../../public/generated/week-01-lecture-03/slide-013.png)

## Explanation

Layering divides a complex problem into smaller tasks, where each layer has a focused responsibility. A layer can use the service below it without needing to understand all of its internal details.

The postal example models network communication: Mia writes the letter, encrypts it and puts it in an envelope, postal workers label and route it, and a truck or airplane physically transports it.

## Walkthrough

The process can be read as a stack of responsibilities:

1. Create the message.
2. Add protection or packaging.
3. Add the destination address and arrange delivery.
4. Transport the item over the physical route.

At the receiver, the steps are performed in reverse: transport delivers the envelope, postal handling uses the address, the protection is removed, and the recipient reads the message.

## Connections and exam relevance

Computer networks use the same idea: application data is handled by higher layers, while lower layers package, address, route, and physically transmit it. Layering makes network design modular and easier to change or troubleshoot.

## Check your understanding

In the postal analogy, step 3 is responsible for adding the destination address and routing the envelope. Separating this from writing and protecting the letter lets each part focus on one responsibility.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 13]
