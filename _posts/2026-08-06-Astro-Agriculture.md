---
layout: post
title: Astro Agriculture - Barman Robotics Lab
---

## Introduction
One of my many projects at the lab was designing instrumentation for our innovative synthetic soil. To accurately track the plant's progress, we would need data on its environment.
Over the course of a few months, I installed and implemented a suite of sensors on a Raspberry Pi and deployed a live web server to visualize the data. 

---
## The sensors
-Temperature  
-Humidity  
-Co2  
-Voc  
-pH  
-Pressure  
-Weight (load cell)  

---
The challenge of this project was integrating everything. It's not hard to read one sensor and publish it to the dashboard, but when there are many, it can be easy to get lost in the sauce.
Therefore, I learned the importance of creating an organized code base and committing to Git often.

This was the first time I worked with a Raspberry Pi, and it was an overall smooth experience. It was cool being able to access the peripheral pins and still having a Linux OS.

---
## Final Results
![Alt Text]({{ "/assets/webUIcamera.png" | relative_url }})
![Alt Text]({{ "/assets/webUIcharts.png" | relative_url }})
![Alt Text]({{ "/assets/webUIreadings.png" | relative_url }})
![Alt Text]({{ "/assets/plantmodule.png" | relative_url }})
