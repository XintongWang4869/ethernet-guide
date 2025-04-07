---
title: The Ethernet Standards
linkTitle: The Ethernet Standards
# description: 
categories: [Networking]
tags: [Ethernet Standards]
weight: 3 
---

{{% pageinfo %}}
"Man is something that shall be overcome. What have you done to overcome him?" (_Thus Spoke Zarathustra_, Nietzsche)
{{% /pageinfo %}}


## Overview of Ethernet Standards

**IEEE**, short for Institute for Electrical and Electronics Engineers, is an institute that develops standards in many industries, and the Ethernet standards are developed by **IEEE-SA**, IEEE Standards Association. Today, **IEEE 802.3** serves as the standard that defines Ethernet protocols, providing the foundation for modern wired network communications.

The goal of this standardization is to ensure equipments are compatible (inter-operation), so as to expand marketplace and benefit both manufacturers and consumers. Therefore, devices not specified within the IEEE 802.3 standard are typically vendor-specific.



### IEEE Supplements

A letter designation is used to address different types of media and technologies used in Ethernet networks. For example:

| Supplement| Description         |
|-----------|-----------------|
| 802.3u-1995   |100BASE-T Fast Ethernet and Auto-Negotiation       |
| 802.3z-1998   | 1000BASE-X Gigabit Ethernet over fiber optic cables   |
| 802.3ab-1999   | 1000BASE-T Gigabit Ethernet over twisted-pair cables  |
| 802.3az-2010  |Energy-Efficient Ethernet


Note that standards developing and publishing lags behind the innovation, especially in the field of computer networking. Therefore, it's possible, and not necessarily a drawback, for a product to be built to draft standards.


## IEEE Media System Identifiers

There are three key components of identifiers:
- **Speed**: indicates the data transmission rate, such as 10 Mbps, 100 Mbps, or 1 Gbps
- **Type of signaling**: indicates the transmission method, such as baseband signaling or encoding schemes
- **Physical medium**: indicates the type of cable, such as twisted-pair, fiber optic, or coaxial cable

The following table provides a detailed breakdown of these identifiers and their meanings:

| Media Systems | Details   |
|-----------|-----------------|
|10BASE5 |<li> 10 megabits per second (Mb/s) transmission speed</li><li>**"BASE": Baseband transmission**, where the entire bandwidth of the physical medium is exclusively used to transmit Ethernet signals.</li><li> 500-meter max length</li>&rarr; Thick Ethernet, using thick coaxial cables for data transmission |
|10BASE2 |<li> 10 Mb/s transmission speed</li><li>Baseband transmission</li><li> 185-meter max length (round to 2) </li> &rarr; Thin Ethernet (Cheapernet), using thinner coaxial cables compared to 10BASE5    |
|10BASE-T |<li> 10 Mb/s transmission speed</li><li>Baseband transmission</li><li>**A hyphen, "-", is used to distinguish the older "length" designators from the newer "media type" designators.**</li><li>**"T":  Twisted-pair wiring** (2 pairs, CAT 3 or better) </li>    |
|100BASE-X |<li> **100 Mb/s (Fast Ethernet)** transmission speed</li><li>Baseband transmission</li><li> **"X": Use of a blocking encoding scheme**</li> &rarr; Includes both 100BASE-TX and 100BASE-FX, based on the same 4B/5B block signal encoding system    |
|100BASE-TX|<li> 100 Mb/s transmission speed</li><li>Baseband transmission</li><li> Twisted-pair wiring (over 2 pairs of CAT 5 cables)</li>&rarr; Mostly used variety of Fast Ethernet  |
|100BASE-FX |<li> 100 Mb/s transmission speed</li><li>Baseband transmission</li><li> **"F": Fiber optic cable** (multimode) </li>      |
|1000BASE-SX |<li> **1000 Mb/s (Gigabit Ethernet)** transmission speed</li><li>Baseband transmission</li><li> **"S": Short-wavelength** fiber optic media segments  |
|1000BASE-LX |<li> 1000 Mb/s transmission speed</li><li>Baseband transmission</li><li> **"L": Long-wavelength** fiber optic media segments  |
|1000BASE-T |<li> 1000 Mb/s transmission speed</li><li>Baseband transmission</li><li> Twisted-pair wiring (over CAT 5 or better) </li> <li>It is based on different signal encoding scheme, compared to the above Gigabit Ethernet systems. </li>  |
|10GBASE-SR |<li> 10 Gb/s Ethernet transmission speed</li><li>Baseband transmission</li><li> **"SR": Short-range** multi-mode fiber optic cable </li>  |
|10GBASE-LR |<li> 10 Gb/s Ethernet transmission speed</li><li>Baseband transmission</li><li> **"LR": Long-range** multi-mode fiber optic cable </li>  |
|10GBASE-T|<li> 10 Gb/s transmission speed</li><li>Baseband transmission</li><li> Twisted-pair wiring (over CAT 6A or better)</li>
|40GBASE-SR4|<li> 40 Gb/s transmission speed</li><li>Baseband transmission</li><li> Over 4 short-range multi-mode fiber optic cable </li>  |
|40GBASE-LR4|<li> 40 Gb/s transmission speed</li><li>Baseband transmission</li><li> Over 4 wavelengths carried by a single long-distance single-mode fiber optic cable </li>  |
|100GBASE-SR10|<li> 100 Gb/s transmission speed</li><li>Baseband transmission</li><li> Over 10 short-range multi-mode fiber optic cable </li>  |
|100GBASE-LR4|<li> 100 Gb/s transmission speed</li><li>Baseband transmission</li><li> Over 4 wavelengths carried by a single long-distance single-mode fiber optic cable </li>  |




<br>

<br>