---
title: The Ethernet System
linkTitle: The Ethernet System
# description: 
categories: [Networking]
tags: [Ethernet]
weight: 4
---


{{% pageinfo %}}
"Man is something that shall be overcome. What have you done to overcome him?" (_Thus Spoke Zarathustra_, Nietzsche)
{{% /pageinfo %}}


## Half-Duplex and Full-Duplex Modes

Previously, before the emergence of Ethernet switches, **half-duplex mode** is the typical operation for Ethernet devices. 

In half-duplex mode:

* Multiple computers communicate over a single Ethernet channel via the **{{< tooltip text="CSMA/CD MAC protocol" key="CSMA/CD" >}}**.   
* A station (ie., the networked device) first listens to the channel, and if the channel is idle, the station transmits its data (Ethernet frames).
* Only one station can send data over the Ethernet channel at any given time.  
* Data transmission rate: 10 Mb/s or 100 Mb/s


Nowadays, **full-duplex mode** is widely adopted by Ethernet devices and is typically enabled through the **{{< tooltip text="Auto-Negotiation" key="AN" >}}** protocol.

In full-duplex mode:

* Each station connected to a switch port does not share the Ethernet channel bandwidth on that link with any other computer.
* Devices can send and receive data simultaneously.  




## The Four Basic Elements of Ethernet

* **The Ethernet frame** — A standardized set of bits

* **The Media Access Control protocol (MAC)**   — A set of rules embedded in each Ethernet interface that allow Ethernet stations to access the Ethernet channel, in either half-duplex or full-duplex mode

* **The signaling components**  — Standardized electronic devices that send and receive signals over an Ethernet channel

* **The physical medium**  — The cables and other hardware used to carry the digital Ethernet signals between computers attached to the network

    
{{% alert title="Note" %}}The Ethernet standard uses "frame", while "packet" is used to describe the data transmitted at Layer 3 (the network layer), by those who wish to differentiate Layer 2 and Layer 3 functions.{{% /alert %}}

<br>

<br>




