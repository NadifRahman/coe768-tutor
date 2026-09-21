---
slide_id: "week-02-lecture-02-slide-019"
source_id: "week-02-lecture-02"
page: 19
week: 2
status: understood
concepts: [mac-address-format, oui, hardware-addressing]
---

# Slide 19

![Original slide 19](../../../public/generated/week-02-lecture-02/slide-019.png)

## Explanation

A MAC address (Media Access Control address) is a link-layer hardware identifier associated with a network interface. A standard MAC address is 48 bits long and is commonly written as 12 hexadecimal digits, for example `01:23:45:67:89:AB`. [week-02-lecture-02, p. 19]

## Walkthrough

Each hexadecimal digit represents four bits, so 12 hexadecimal digits represent 48 bits. The first 24 bits commonly identify the organization/manufacturer prefix, known as the OUI, and the remaining bits identify the interface within that allocation. The address is intended to be unique among interfaces.

## Connections and exam relevance

The slide describes MAC addresses as permanently programmed by manufacturers. More precisely, an interface usually has a factory-assigned burned-in address, but software can sometimes override or spoof the address, and some modern systems use randomized MAC addresses for privacy. For normal networking analysis, use the factory-assigned address as the interface's identity on the local link. [week-02-lecture-02, p. 19]

## Check your understanding

How many bits are in a standard MAC address, and how many hexadecimal digits are normally used to write it?

Student response: A standard MAC address is 48 bits, normally written as 12 hexadecimal digits.

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-02, p. 19]
