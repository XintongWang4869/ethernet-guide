---
title: The OSI Model
linkTitle: The OSI Model
categories: [Networking]
tags: [Ethernet, OSI Model]
weight: 2
---


{{% pageinfo %}}
"Man is something that shall be overcome. What have you done to overcome him?" (_Thus Spoke Zarathustra_, Nietzsche)
{{% /pageinfo %}}



## Open Systems Interconnection (OSI)

The Open Systems Interconnection (OSI) reference model is a conceptual framework that divides network operations into seven layers:


<figure style="display: flex; flex-direction: column; align-items: center; text-align: center;">
  <img src="osi-model-1.svg" alt="OSI Model" style="max-width: 100%;">
  <figcaption style="font-style: italic; color: gray;">OSI Model</figcaption>
</figure>

* **Application Layer:**
    * Provides ​network services directly to end-user applications, how?
        * User interface
        * Specific rules (protocols) for different apps
        * Data semantics
* **Presentation Layer:**   
    * Ensures data sent by one application can be correctly interpreted by another<sup>1</sup>, and also ensures secure<sup>2</sup>, and efficient communication<sup>3</sup>:
        1. Data format conversion
        2. Data encryption/decryption
        3. Data compression

* **Session Layer:**
    * Manages and controls connections (ie, sessions) between applications     

* **Transport Layer:** 
    * Provides end-to-end error recovery mechanisms
        - TCP (Transmission Control Protocol) for accurate communication
        - UDP (User Datagram Protocol) for fast communication

* **Network Layer:** 
    * Establishes communications across different networks
        - Logical addressing: assigns unique IP addresses to devices
        - Routing: finds the best path for data to travel between source and destination

* **Data Link Layer:** 
    * Ensures ​reliable data transfer between devices within the same network (LAN)
    * Has two sublayers:  
        * Logical Link Control (LLC)   
        * Media Access Control (MAC) 
    ![DDL Sublayers](./osi-model-2.svg)

* **Physical Layer:** 
    * Defines how data is transmitted as:
        * Electrical signals over copper cables
        * Optical signals over fiber
        * Radio signals over radio waves






## Example Scenario

To better understand the networking functions of each layer, here is a step-by-step breakdown of the process. The scenario involves a user typing `www.example.com` in a web browser and pressing "Enter", attempting to fetch the webpage from the remote server:

1. Application Layer (Layer 7)  

    The user browser generates an ​HTTP/HTTPS GET request for `www.example.com`, during which a **{{< tooltip text="DNS (Domain Name System)" key="DNS" >}}** server is used to resolve `www.example.com` to an IP address, such as `192.168.1.1` ({{< tooltip text="IPv4" key="IPv4" >}}).

2. Presentation Layer (Layer 6) 

    Before transmission, encrypt the request with TLS (Transport Layer Security) if the sites uses HTTPS. The data is compressed.

3. Session Layer (Layer 5)   

    A session is established between the user browser and the server, to handle authentication and persistent connections.

4. Transport Layer (Layer 4)  

     Transmission Control Protocol (TCP) is used in this case for connection-oriented, reliable delivery. Data is broken into ​segments (TCP Header + payload) for transmission.

5. Network Layer (Layer 3)     

    The segments are further packed into IP packets (IP Header + payload). Routing is based on IP addresses, which are obtained by querying a DNS (Domain Name System) server.

6. Data Link Layer (Layer 2)   

    The IP packet is wrapped inside an **Ethernet frame** (MAC Header + payload + Trailer), which adds the source and destination MAC addresses, to be transmitted between devices on the ​same local network. The Ethernet frame is sent from the user computer to the router.     
    
    {{% alert title="Note" %}}If the user is using WI-FI instead of wired Ethernet, the IP packet is wrapped inside Wi-Fi frames, which will then be converted into ​radio signals in the Physical Layer..{{% /alert %}}


7. Physical Layer (Layer 1)

    Ethernet frames are converted into ​bits (0s and 1s) and transmitted via ​electrical signals (over copper) or ​light pulses (fiber).

8. On the server side:  

    &rarr; Converts the bitstream into structured ​Ethernet frames. 

    &rarr; Checks the ​destination MAC address and validates the frame’s integrity.   

    &rarr; Strips the Ethernet header/trailer and reads the IP packet.   

    &rarr; Verifies the IP address and passes the TCP segment to the Transport Layer.   

    &rarr; Checks for errors and passes the reassembled data stream to the Application Layer.  

    &rarr; Processes the HTTP request and fetches the requested resource (in this case, it is the web page).  

    &rarr; Sends back an HTTP response, which is broken into TCP segments  &rarr;  ​Encapsulated into IP packets &rarr;  ​Wrapped in new Ethernet frames &rarr;  ​Transmitted as bits back to the client.



## Role of Ethernet


From the above example, we can identify the role of Ethernet in the following aspects:

* **Local Communication:** Ethernet handles data transfer between devices on the same network (in this example, the user's computer and the router).
* **MAC Addressing:** Ethernet uses MAC addresses to uniquely identify devices on a ​local network, ensuring frames reach the correct device on the LAN.
* **​Error Detection:** The Frame Check Sequence (FCS) in Ethernet frames verifies data integrity.


Although the OSI model is not an architecture or blueprint for network design, the OSI model provides a common organizational scheme for network standardization.




