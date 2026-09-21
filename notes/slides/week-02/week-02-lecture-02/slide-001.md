---
slide_id: "week-02-lecture-02-slide-001"
source_id: "week-02-lecture-02"
page: 1
week: 2
status: understood
concepts: [reference-models, osi-model]
---

# Slide 1

![Original slide 1](../../../public/generated/week-02-lecture-02/slide-001.png)

## Explanation

This slide introduces the central purpose of a reference model: deciding how a network's work should be divided into layers and which functions belong in each layer. The OSI (Open Systems Interconnection) model is a seven-layer conceptual framework developed by ISO in 1984. Each layer has a defined role, and the layers cooperate to move data between hosts. It is a model for describing and reasoning about networks; it is not a claim that every real network is implemented as seven separate physical components. [week-02-lecture-02, p. 1]

## Walkthrough

Think of sending a message from one host to another. Instead of treating “networking” as one giant task, we divide it into responsibilities. Each layer handles a particular part and relies on the layer next to it. This separation makes the system easier to design, explain, replace, and troubleshoot. The rest of this lecture will identify the seven layers and the responsibilities associated with them. [week-02-lecture-02, p. 1]

## Connections and exam relevance

This directly extends the earlier idea of layering and modularity: a reference model gives names and boundaries to the modules. In exams, distinguish “OSI model” from “the exact protocols used by the Internet.” OSI is primarily a conceptual/reference framework; the Internet protocol suite is commonly described with a different practical layer grouping. [week-02-lecture-02, p. 1]

## Check your understanding

Why is the OSI model described as a **conceptual framework** rather than as seven physical devices that every network must contain?

Student answer: It is a conceptual framework for reasoning about how networking can be layered and how responsibilities can be abstracted; it does not require every implementation to follow the seven layers exactly.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 1]
