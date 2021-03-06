# Computer Networks

A **computer network** is a "system (of) connect(ed) computers and (computer hardware)"
 which use "communications media" to transmit data
  to other members in the network.

## Network Communications Media

**Communications media** refer to the pathways, or methods, by which data are transmitted.
 Cable media transmit information over physical wires or cables, whereas broadcast media transmit information through electromagnetic waves.

### Cable Media

Cable media are described by their physical composition and each have advantages and disadvantages in terms of capability and cost.

**Twisted pair wire** is a medium comprised of "twisted copper wires" which is commonly used to "transmit business telephone communications".
 Twisted-pair wire is inexpensive, but "slow ... and subject to (intrusion and) interference."

**Coaxial cable** is a medium comprised of "insulated copper wire"
 and is commonly used to "transmit high-speed data traffic and television signals". Cable is "less susceptible to interference" but "more expensive and harder to work with" than twisted-pair wire.

**Fiber-optic cable** is a medium comprised of "thin ... glass fibers that transmit information via light pulses generated by lasers". Fiber provides a significant increase in bandwidth and security, but may involve great up-front investment costs, and is "harder to work with" than other cable media.

### Broadcast Media

Examples include:

 + Bluetooth
 + WiFi
 + Wireless Mesh Networks
 + Cellular radio
 + Satellite radio
 + Wireless Broadband

## Network Sizes

Computer networks are often described in terms of size:

network size | description | example(s)
--- | --- | ---
Personal Area Network (PAN) | Two ore more devices in a very limited geographical region, usually within the same room | a bluetooth connection between headphones and mobile phone
Local Area Network (LAN) | "two or more devices in a limited geographical region, usually within the same building" | a home WiFi network
Wide Area Network (WAN) | "covers a large geographic region; typically connects multiple LANs" | a university network; the Internet

## The Internet

The **Internet** is a very very large WAN computer network. It is a network of networks.

![an example internet backbone](http://www.nthelp.com/images/sprint.jpg)

### Internet Protocols

Computers connected to the Internet communicate according to a "common set of rules and procedures", or protocols. The following table identifies some of them:

abbreviation | name | description
--- | --- | ---
[HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol)  | Hyper Text Transfer Protocol | The foundation protocol for the Internet.
[HTTPS](https://en.wikipedia.org/wiki/HTTPS)  | Secure Hyper Text Transfer Protocol | A widely-used Internet protocol for secure network communication over HTTP within a connection encrypted by SSL/TLS.
[SSL/TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security) | Transport Layer Security (formerly and still known as Secure Sockets Layer) | For providing communication security over a network.
[TCP/IP](#https://en.wikipedia.org/wiki/Transmission_Control_Protocol) | Transmission Control Protocol, which compliments the Internet Protocol | Provides reliable, ordered, and error-checked delivery of a stream of octets between applications running on hosts communicating over an IP network.
[FTP](https://en.wikipedia.org/wiki/File_Transfer_Protocol) | File Transfer Protocol | For transmitting large files between computers.
[SMTP](https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol) | Simple Mail Transfer Protocol | For transmitting electronic mail between computers.
[SSH](https://en.wikipedia.org/wiki/Secure_Shell) | Secure Shell | A cryptographic (encrypted) network protocol to allow remote login and other network services to operate securely over an unsecured network.
[SFTP](https://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol) | SSH/Secure File Transfer Protocol | For transferring files over SSH.

When computers communicate information over the Internet, they do so according to a set of rules or standards set forth by these protocols. The Internet Protocol primarily governs the routing and delivery of information from one computer to another.

Computers participating in these connections each have an address, or location where the information is sent and received. Just as a street address identifies a building within a connected system of roads and highways, and as a telephone number identifies a phone's connection to a cellular network, an **Internet Protocol (IP) Address** identifies a computer's connection to the Internet. IP Address notation typically includes numbers separated by decimals in IP Version 4 (e.g. *144.228.10.74*), and numbers or letters separated by colons in IP Version 6 (e.g. *2601:37b:c211:7109:7833:f6d1:1f15:9174*).

When information is traveling throughout the network, data is separated into component parts and encapsulated into **packets** which also contain routing information. These packets may or may not take the same route across the network and may or may not arrive at the destination at the same time. Once all the packets are received, they are re-assembled into the original information representation.

### Internet Architecture

#### Peer-to-Peer

In **Peer-to-peer (P2P)** networks, connected computers share the same or similar information-sharing responsibilities. Napster, Kazaa, and BitTorrent are examples of a popular P2P sites.

#### Client/Server

Within the context of today's Internet, most computers connect according to **Client/Server** architecture. The role of the client computer is to request information, whereas the responsibility of the server is to fulfill those requests.

##### Lifecycle of a Network Request

The way you are most likely familiar with requesting information over the Internet is by visiting a URL in your web browser. In this case, your computer is the client making the request for information. And the computer hosting the website associated with the given URL is the server.

  1. The client sends a request to the server.

  1a. If the client doesn't know the IP address of the server, it will ask a **Domain Name System (DNS) Server** to lookup the IP address associated with that URL's domain name. In this way, the role of the DNS is analogous to the role of the telephone operator when you dial *411*, in which you may ask the operator, "May I please have the number for Pepe's Pizza in New Haven?" and the operator would either share the phone number with you, or connect your call directly.

  2. The server receives the request, processes it, and sends a response back to the client.

  3. The client receives the response, and within the context of the web-browsing example, the client's web browser interprets and formats the results on screen.

##### Client-side vs Server-side Programming

You may have heard references to client-side and/or server-side programming. You can generally think of **server-side** software as a set of instructions executed by the server, and **client-side** software as a set of instructions executed by the client.

Practically, server-side applications are responsible for processing web requests into responses. Written in server-side programming languages like [Ruby](https://www.ruby-lang.org/en/), [Python](https://www.python.org/), [PHP](http://php.net/), etc., they often handle database connections, translating database data into HTML or JSON responses. A web service (i.e. [RESTful API](https://en.wikipedia.org/wiki/Representational_state_transfer#Applied_to_Web_services)) is a perfect example of a purely server-side application.

Client-side applications are generally responsible for displaying or otherwise representing the information returned by server-side applications. Written in client-specific languages like [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript), they are commonly executed within web browsers or native applications. They may provide user interactivity or other functionality that does not require subsequent communication with the server after the server's initial response. Or they may send information back and forth to and from the server multiple times within a single user session. Web pages and data visualizations are good examples of client-side web applications.

In some cases, a single web application may contain both server-side and client-side logic. This hybrid approach is exemplified by any fully-functional [Model-View-Controller (MVC)](https://developer.apple.com/library/content/documentation/General/Conceptual/DevPedia-CocoaCore/MVC.html) application built using the [Ruby on Rails](http://rubyonrails.org/) or [Python Django](https://www.djangoproject.com/) framework. In other cases, client-side logic and server-side logic may be separated into different web applications (i.e. a back-end web service distinct from a front-end user interface).




















<hr>

Reference:

 + Intro to Information Systems, Rainer, 5th edition, ISBN 9781118674369
 + Quotes based on Rainer 4.5, 6.1, 6.2 unless otherwise noted

Additional Resources:

 + http://fcit.usf.edu/network/chap1/chap1.htm
 + http://fcit.usf.edu/network/chap4/chap4.htm
 + https://en.wikipedia.org/wiki/Computer_network
 + http://study.com/academy/lesson/types-of-networks-lan-wan-wlan-man-san-pan-epn-vpn.html
 + http://www.edinformatics.com/inventions_inventors/fiber_optics.htm
 + http://fcit.usf.edu/network/chap2/chap2.htm
 + http://flask.pocoo.org/docs/0.10/htmlfaq/
 + https://en.wikipedia.org/wiki/Lists_of_network_protocols
 + https://en.wikipedia.org/wiki/Internet_Protocol
 + http://www.livinginternet.com/i/iw_arch.htm
 + https://www.godaddy.com/help/what-is-dns-665
 + https://www.techopedia.com/definition/454/peer-to-peer-architecture-p2p-architecture
 + http://www.cs.ccsu.edu/~stan/classes/cs490/slides/networks4-ch2-4.pdf
 + https://www2.cs.sfu.ca/~ggbaker/zju/web/
 + https://www.washington.edu/accesscomputing/webd2/student/index.html
 + https://web.stanford.edu/class/msande91si/www-spr04/readings/week1/InternetWhitepaper.htm
 + http://docs.webplatform.org/wiki/concepts/Internet_and_Web/How_does_the_Internet_Work
 + http://www.theshulers.com/whitepapers/internet_whitepaper/index.html
