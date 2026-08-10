---
layout: post
title: Astro Agriculture - Barman Robotics Lab
---

## Introduction
One of my many projects at the lab was designing instrumentation for our innovative experimental plant-growth substrate. The goal was to monitor the plant's environment over time so we could evaluate water usage, transpiration behavior, growth conditions, and overall system performance.

Over the course of a few months, I integrated multiple environmental sensors with a Raspberry Pi, built a Python-based data logger, stored timestamped readings in a database, and deployed a local Flask dashboard for real-time visualization.

---
## The sensors
The following sensors were used:

| Sensor | Measurement | Purpose |
|---|---|---|
| SHT30 | Temperature and humidity | Growth environment and transpiration conditions |
| SCD31 | CO₂ | Photosynthesis and respiration environment |
| BME680 | Pressure and VOCs | Air quality and environmental monitoring |
| Phidget 1 kg load cell | Weight | Water loss and plant mass changes over time |
| Atlas Scientific EZO pH | pH | Water acidity |

---
## System Architecture
The system was built around three main components:

- **Logger:** A Python polling loop that reads each sensor every 30 seconds.
- **Database:** Stores each sensor reading with a timestamp and ID.
- **Flask Server:** Reads the latest database entries and serves them to a local web dashboard.

I intentionally separated the logger from the web server so that the system would be more fault-tolerant. If the dashboard crashed, the logger could continue collecting data. If the logger stopped, the dashboard could still display the most recent stored readings.
![instrumentation architecture]({{ "/assets/instrumentation_architecture.png" | relative_url }})

---
## Takeaways
The challenge of this project was integrating everything. It's not hard to read one sensor and publish it to the dashboard, but when there are many, it becomes easy to get lost.
Therefore, I learned the importance of creating an organized code base and committing to Git often.

This was the first time I worked with a Raspberry Pi, and it was an overall smooth experience. It was cool being able to access the peripheral pins and still having a Linux OS.

---
## Final Results
The final system collected timestamped sensor readings every 30 seconds and displayed both live values and historical trends through the dashboard.
![Dashboard camera tab]({{ "/assets/webUIcamera.png" | relative_url }})
![Dashboard charts tab]({{ "/assets/webUIcharts.png" | relative_url }})
![Dashboard readings tab]({{ "/assets/webUIreadings.png" | relative_url }})
![Plant growth module]({{ "/assets/plantmodule.jpeg" | relative_url }})
