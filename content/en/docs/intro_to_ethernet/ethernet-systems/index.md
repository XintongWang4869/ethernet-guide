---
title: Ethernet System
linkTitle: Ethernet System
# description: 
categories: [Networking]
tags: [Ethernet]
weight: 8
---


{{% pageinfo %}}
"Man is something that shall be overcome. What have you done to overcome him?" (_Thus Spoke Zarathustra_, Nietzsche)
{{% /pageinfo %}}


## The Ethernet System

* Before:   
    **Half-duplex mode**: typical operation for Ethernet devices (before Ethernet switches)

    * Multiple computers communicate over a single Ethernet channel via the CSMA/CD MAC protocol.   
    * Only one computer can send data over the Ethernet channel at any given time.  
    * A station first listens to the channel, and if the channel is idle, the station transmits its data (Ethernet frames).
    * Speed: 10 and 100 Mb/s



* These days:  
    **Full-duplex mode**: selected with Auto-Negotiation protocol

    * Devices can send and receive data simultaneously.  
    * Each station connected to a switch port does not share the Ethernet channel bandwidth on that link with any other computer.
