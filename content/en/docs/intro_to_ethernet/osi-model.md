---
title: OSI Model
linkTitle: OSI Model
# description: 
weight: 2
---


{{% pageinfo %}}
"Man is something that shall be overcome. What have you done to overcome him?" (_Thus Spoke Zarathustra_, Nietzsche)
{{% /pageinfo %}}



## Open Systems Interconnection (OSI)

The Open Systems Interconnection (OSI) reference model is a conceptual framework that divides network operations into seven layers:

<img src="/content/basics/osi-model.svg" alt="OSI Model">


## Example

Here is a step-by-step breakdown of the process, following the OSI model, to help you better understand the networking functions. The scenario involves a user typing "www.example.com" into a web browser and pressing "Enter", attempting to fetch the webpage from the remote server:

1. Application Layer (Layer 7)  

    The user browser generates an ​HTTP/HTTPS GET request for www.example.com, during which a DNS (Domain Name System) server is used to resolve www.example.com to an IP address.

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
    
    > If the user is using WI-FI instead of wired Ethernet, the IP packet is wrapped inside Wi-Fi frames, which will then be converted into ​radio signals in the Physical Layer. 

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




