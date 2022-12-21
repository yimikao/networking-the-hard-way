# PROTOCOLS

## ISO OSI Protocol
Abandoned for TCP/IP Model/Protocol instead

```
Application
    /\
    ||
    \/
Presentation
    /\
    ||
    \/
Session
    /\
    ||
    \/
Transport
    /\
    ||
    \/
Network
    /\
    ||
    \/
Data Link
    /\
    ||
    \/
Physical
```


## TCP/IP PROTOCOL

These have been immensely successful and have led to The Internet.

```
Application  ============= OSI 5 - 7
    /\
    ||
    \/
TCP / UDP  ============= OSI 4
    /\
    ||
    \/
    IP  ============= OSI 3
    /\
    ||
    \/
H/W interface ============= OSI 1 - 2
```

# NETWORKING

A network is a `communications system` for `connecting` end systems called `hosts`. The `mechanisms of connection` might be copper wire, Ethernet, fiber optic, or wireless, but that won’t concern us here. A **local area network (LAN)** connects computers that are close together, typically belonging to a home, small organization, or part of a larger organization. There are other like WAN, MAN etc.

An internet (lower-case) is a connection of two or more distinct networks, typically LANs or WANs. An intranet is an internet with all networks belonging to a single organization.
There are significant differences between an internet and an intranet. Typically, an intranet will be under a single administrative control, which will impose a single set of coherent policies. An internet, on the other hand, will not be under the control of a single body, and the controls exercised over different parts may not even be compatible.

A trivial example of such differences is that an intranet will often be restricted to computers by a small number of vendors running a standardized version of a particular operating system. On the other hand, an internet will often have a smorgasbord of different computers and operating systems.
The techniques of this book are applicable to internets. They are also valid with intranets, but there you will also find specialized, non-portable systems.
And then there is the “mother” of all internets: The Internet. This is just a very, very large internet that connects us to Google, my computer to your computer, and so on.


# GATEWAYS

A gateway is a generic term for an entity used to connect two or more networks.


# Packet Encapsulation


The communication between layers in either the OSI or the TCP/IP stacks is done by sending packets of data from one layer to the next, and then eventually across the network. Each layer has administrative information that it has to keep about its own layer. It does this by adding header information to the packet it receives from the layer above, as the packet passes down. On the receiving side, these headers are removed as the packet moves up.
For example, the TFTP (Trivial File Transfer Protocol) moves files from one computer to another. It uses the UDP protocol on top of the IP protocol, which may be sent over Ethernet. 


# Connection Models

In order for two computers to communicate, they must set up a path whereby they can send at least one message in a session. There are two major models for this:

- Connection oriented

A single connection is established for the session. Two-way communications flow along the connection. When the session is over, the connection is broken. The analogy is to a phone conversation. An example is TCP


- Connectionless

In a connectionless system, messages are sent independent of each other. Ordinary mail is the analogy. Connectionless messages may arrive out of order. An example is the IP protocol. UDP is a connectionless protocol above IP and is often used as an alternative to TCP, as it is much lighter weight.

