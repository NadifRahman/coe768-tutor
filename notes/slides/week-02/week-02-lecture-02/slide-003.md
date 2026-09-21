---
slide_id: "week-02-lecture-02-slide-003"
source_id: "week-02-lecture-02"
page: 3
week: 2
status: understood
concepts: [application-layer-services, application-protocols]
---

# Slide 3

![Original slide 3](../../../public/generated/week-02-lecture-02/slide-003.png)

## Explanation

The application layer is the top layer of the OSI model and contains many application-level protocols. A user program such as a web browser is not itself “the application layer”; instead, it uses application-layer protocols such as HTTP to perform communication functions. The slide gives file transfer, Google search, and e-business as examples of services supported through this layer. [week-02-lecture-02, p. 3]

## Walkthrough

For a web request, the browser creates or requests data, then uses HTTP to format the request and communicate its application-level meaning. HTTP passes the resulting data to the presentation layer, which is directly below it in the OSI stack. The application layer is therefore about what the communicating applications want to accomplish—such as retrieving a web page or transferring a file—not about moving electrical or radio signals. [week-02-lecture-02, p. 3]

## Connections and exam relevance

This clarifies a common distinction: an **application** is a program, while an **application protocol** is an agreed set of message formats and rules that programs use. A browser may use HTTP, but HTTP itself is not the browser. The lower layers provide the transport and delivery mechanisms that HTTP relies on. [week-02-lecture-02, p. 3]

## Check your understanding

Is a web browser itself an application-layer protocol, or is it an application that uses a protocol? What role does HTTP play?

Student response: A browser is an application; HTTP is the protocol it uses to exchange web data.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 3]
