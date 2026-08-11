---
layout: post
title: CAN bus Charger Communication - Barman Robotics Lab
---

## Introduction
An autonomous drone system needs a autonmous robus and safe charging system to go with it.  

One of my projects at the lab was building communication between our drone system and its charger. Being able to turn the charger on and off, set charging curves, read faults and relevant data is essential. Additionally, with this capability, we can then establish autonomous charging sequences, remote monitoring and integration with drone landing.  

The charger uses the CAN bus protocol to communicate. With a CAN bus hardware module, we can write code to be able to read and write to the charger.  

Over a few weeks, I tested CAN bus communication with the charger, built a Python interface, and added support for reading status information and sending basic control commands.  

---
## Development
I ordered a USB-CAN adapter that is compatible with socket can which means we can use the python-can library to read and write messages. Since reading and writing messages involve knowing the address, packet size and manipulating the data in such a way the charger can understand it takes a lot of messy code to read or write a simple value. Hence, a library would abstract away the messy code into neat commands reducing repeated code and making it easier to use in high level scripts. 

The library has the following capabilities:  
- Turn charger on/off
- Read output voltage/current
- Read temperature
- Read manufacturer
- Read fault/status flags
- Read/write charge curve settings
