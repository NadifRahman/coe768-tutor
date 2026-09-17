---
slide_id: "week-01-lecture-03-slide-032"
source_id: "week-01-lecture-03"
page: 32
week: 1
status: understood
concepts:
  - layering-information-hiding-and-reuse
---

# Slide 32

![Original slide 32](../../../public/generated/week-01-lecture-03/slide-032.png)

## Explanation

Layering hides lower-level implementation details from applications and enables reuse. A web browser does not need to know whether its data is carried by Wi-Fi, Ethernet, or another lower-layer technology.

## Walkthrough

Without information hiding, developers would need to write different web applications for different protocol stacks and network environments. With layering, the same web application can run across different networks because the lower layers provide compatible services through their interfaces.

## Connections and exam relevance

This summarizes the examples from the previous slides: HTTP and TCP can remain the same while the lower link technology changes between Wi-Fi and Ethernet.

## Week 1 exam-review summary

### 1. What a network is

A computer network interconnects computing devices so they can exchange data and provide services. A **node** is a participating device, such as a host, router, or switch. A **host** is an end device that runs applications; a server provides a service and a client requests it. Client and server describe roles in an interaction, not permanent hardware categories.

Networks can be classified by geographic scope:

- **LAN:** local area, such as a home, lab, or office.
- **MAN:** metropolitan area, such as a city.
- **WAN:** large geographic area connecting networks across regions or countries.
- The Internet is a **network of networks**, not one giant LAN.

Three related perspectives are important:

- **Distributed systems:** applications or services cooperating across multiple computers.
- **Computer networks:** how devices are connected and how packets move.
- **Communications:** how bits are represented and carried as electrical, optical, or radio signals.

### 2. Fundamental network problems

- **Reliability:** data can be corrupted, lost, or delayed, and devices or routes can fail. Error-detection information can reveal corruption; retransmission, correction, or alternate routes may be needed to recover.
- **Resource allocation:** devices sharing one channel can transmit simultaneously and collide. CSMA/CD detects collisions on classic shared Ethernet; CSMA/CA tries to avoid collisions on Wi-Fi.
- **Flow control:** a sender can overwhelm a receiver's buffer. Stop-and-wait sends a unit and waits; sliding-window methods allow a controlled amount of data in flight.

### 3. Devices and links

- A **link/channel** is the connection between devices: copper, fiber, or wireless medium.
- A **switch** primarily connects devices within one LAN and forwards local Ethernet frames using MAC addresses.
- A **router** connects different IP networks and forwards packets toward the next hop using destination IP information.
- A **hub** is an older shared-medium device that repeats incoming signals to all ports. Every interface can physically observe the frame, but normally only the matching destination MAC accepts it. Switches reduce this unnecessary sharing.
- A consumer **Wi-Fi router** commonly combines a router, wireless access point, Ethernet switch, NAT, DHCP, and firewall. It can bridge Wi-Fi and wired devices within one LAN and route between the home LAN and the WAN/Internet.

Link direction modes:

- **Simplex:** one-way communication only.
- **Half duplex:** both directions are possible, but not simultaneously; Wi-Fi commonly shares a channel this way.
- **Full duplex:** both directions can operate simultaneously.

### 4. MAC addresses, IP addresses, and frames

- A **MAC address** identifies a network interface on the local link. Switches use MAC addresses for local frame delivery. A laptop's Wi-Fi and Ethernet interfaces can have different MAC addresses; a router normally has one per interface.
- An **IP address** is a logical network-layer address used for communication across networks. Routers use the destination IP and routing information to choose a next hop.
- For a remote destination, the destination IP usually remains the final server's IP across the route, while source and destination MAC addresses describe the current link and usually change when a router creates a new frame. NAT can additionally change the source IP.
- An **Ethernet frame** is a link-layer envelope: destination MAC, source MAC, type/length, payload containing an IP packet, and an FCS trailer for error detection.
- A switch normally forwards a frame without changing its MAC addresses. A router removes the old link-layer wrapper and creates a new frame for the next link.
- ARP (IPv4) and Neighbor Discovery (IPv6) can discover a local next-hop link address; these details are useful background but are not the main Week 1 focus.

### 5. Network software, protocols, and diagnostics

- **Wireshark** captures and analyzes packets that are already traveling through a network.
- **Nmap** discovers hosts and services by sending probes.
- **GNS3** simulates networks for testing and troubleshooting.
- A **protocol** is a shared set of rules defining message format, message order, and actions taken during communication.
- A **socket API** is the programming interface through which an application uses transport services. A socket is associated with an IP address, transport protocol, and port.
- **Ports** identify applications or services on a host. Common ranges are well-known/system ports, registered ports, and dynamic/ephemeral ports. A server listens on a port; a client usually receives a temporary source port.
- **Ping** commonly uses ICMP echo request/reply to test reachability and round-trip time.
- **Traceroute** sends probes with increasing TTL values. Each expired TTL can cause an intermediate router to report itself, revealing hops and approximate timing. A destination response indicates arrival; an unreachable response indicates a routing or delivery problem; timeouts can mean filtering, loss, or no response.
- The destination IP generally stays the same while routers make separate next-hop decisions. TTL limits the lifetime of a packet and prevents a persistent routing loop from circulating forever.

### 6. Common application protocols

- **HTTP:** request/response protocol for web pages and web APIs. `GET` requests a resource; `200 OK` means success; `404 Not Found` means the resource was not found.
- **DNS:** maps domain names to IP addresses. It commonly uses UDP because queries are small and frequent, while DNS handles loss through retries, alternate servers, caching, and TCP fallback when needed. DNS over TLS/HTTPS uses stream-based transports.
- **DHCP:** automatically provides a device with an IP address, gateway, and DNS-server information when it joins a network.
- **FTP:** transfers files; SFTP is a different SSH-based protocol.
- **Telnet:** older remote command-line access; insecure and mostly replaced by SSH.
- HTTP, FTP, and Telnet traditionally use TCP; DNS and DHCP commonly use UDP. HTTP/3 is an important modern exception because it uses QUIC over UDP while providing reliability above UDP.

### 7. TCP and UDP

**TCP** is connection-oriented and reliable:

- Establishes a connection before application data.
- Provides ordered delivery, acknowledgments, retransmission, and flow control.
- Uses sequence and acknowledgment numbers to detect gaps and recover missing segments.
- Common control flags include `SYN`, `ACK`, `FIN`, and `RST`.
- The three-way handshake is `SYN → SYN-ACK → ACK`.
- Connection termination uses FIN/ACK exchanges; each direction of TCP's full-duplex stream can close independently.

**UDP** is connectionless:

- Sends datagrams without a TCP-style handshake.
- Has less setup and maintenance overhead.
- Can detect corruption but does not provide built-in retransmission, ordering, or guaranteed delivery.
- The application can add its own recovery if required.

Do not confuse TCP's reliability with HTTP itself: HTTP uses TCP's service, while TCP performs the transport-level recovery.

### 8. Layering and modularity

Layering divides a complex networking problem into smaller responsibilities. A higher layer uses the service of the next lower layer through an interface without needing to know the lower layer's implementation.

- **Adjacent-layer interaction** happens vertically within one host, such as HTTP using TCP.
- **Peer/same-layer interaction** is conceptual communication between corresponding protocols on different hosts, such as browser HTTP and server HTTP.
- Only adjacent layers directly interact inside a host. Actual data travels down the sender's stack, across the medium, and up the receiver's stack.
- Layering provides information hiding and functionality reuse. The same browser can work over Wi-Fi, Ethernet, fiber, or another supported lower-layer technology.

### 9. Encapsulation and decapsulation

As data moves down the sender's stack, each layer adds control information:

```text
Ethernet frame
  [Ethernet header [IP packet [TCP header + HTTP data]] Ethernet trailer]
```

- A **header** is information added before data.
- A **trailer** is information added after data; it may support error detection or correction.
- **Decapsulation** is the reverse process: each receiving layer reads and removes its own wrapper, then passes the remaining data upward.
- TCP handshake messages contain TCP control information but no HTTP data. After the handshake, HTTP data becomes the payload of a TCP segment, which is then carried inside an Ethernet or Wi-Fi frame.

### 10. Protocol stack example to remember

For a browser using Wi-Fi to contact a server using Ethernet:

```text
Browser:   HTTP → TCP → IP → 802.11/Wi-Fi
Router:    IP with 802.11 on one interface and Ethernet on another
Server:    HTTP → TCP → IP → Ethernet
```

The router participates in IP forwarding and the two link layers, but it does not need to run the endpoint's HTTP or TCP application conversation. It decapsulates the incoming Wi-Fi frame, processes the IP packet, and encapsulates that packet in a new Ethernet frame. A consumer Wi-Fi router may also bridge Wi-Fi and wired devices in one LAN; bridging is not the same as routing between different IP networks.

### High-value exam distinctions

- **Switch vs router:** switch forwards within a LAN using MAC; router connects IP networks using destination IP and next-hop decisions.
- **MAC vs IP:** MAC is local-link/interface identification; IP is logical network addressing used across networks.
- **Frame vs packet vs segment:** Ethernet carries a frame; an IP packet is inside the frame; a TCP segment is inside the IP packet; HTTP data is inside the TCP segment.
- **TCP vs UDP:** TCP provides connection-oriented reliable delivery; UDP provides connectionless low-overhead datagrams without built-in recovery.
- **HTTP vs TCP:** HTTP defines application messages; TCP transports them reliably.
- **Encapsulation vs decapsulation:** add wrappers while sending down; remove them while receiving up.
- **Wi-Fi vs Ethernet:** different link/physical technologies can carry the same IP/TCP/HTTP data.
- **Hub vs switch:** hub repeats signals to all ports; switch selectively forwards frames based on learned MAC addresses.

## Check your understanding

Why can the same web application work across both Wi-Fi and Ethernet networks?

<!-- personal:start -->
## Personal notes

<!-- personal:end -->

## Sources

- [week-01-lecture-03, p. 32]
