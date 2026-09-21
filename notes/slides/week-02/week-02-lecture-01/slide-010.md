---
slide_id: "week-02-lecture-01-slide-010"
source_id: "week-02-lecture-01"
page: 10
week: 2
status: unseen
concepts: []
---

# Slide 10

![Original slide 10](../../../public/generated/week-02-lecture-01/slide-010.png)

## Explanation

These are the basic data-transfer operations for an established socket. `write()` copies bytes from the program's buffer toward the socket; `read()` copies available bytes from the socket into the program's buffer [week-02-lecture-01, p. 10].

## Walkthrough

```c
int write(int sockfd, const void *buffer, int len);
int read (int sockfd,       void *buffer, int len);
```

For `write()`, `buffer` points to data to send and `len` is its byte length. The return value is the number of bytes written, or `-1` on error.

For `read()`, `buffer` is the destination memory and `len` is the maximum number of bytes to copy. The return value is the number of bytes read; `0` means the peer has closed its sending side, and `-1` means an error.

Because TCP is a byte stream, one `write()` is not guaranteed to correspond to one `read()`. A receiver may get only part of a logical message and must keep reading until it has enough bytes according to the application's framing rule, such as a fixed length, delimiter, or length prefix.

## Connections and exam relevance

This is where the connected descriptor returned by `accept()` becomes useful. The most important reasoning skill is interpreting return values and remembering that TCP provides bytes, not message boundaries [week-02-lecture-01, p. 10].

## Check your understanding

If a client writes 100 bytes, is the server guaranteed to receive all 100 bytes in one `read()` call? What should the server do if it receives only 40?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-02-lecture-01, p. 10]
