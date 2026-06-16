---
layout: post
title: LED Music Sync
---

For my final project for JHU Mastering Electronics Lab (EN.520.231), I built an LED music sync, a circuit with LEDS that react dynamically to sound.
Based on the frequency of the music, different LEDs light up, creating a visual companion to the audio.

---
## Implementation Overview
A microphone captures audio input and then passes it through a series of filters and Op-Amps, isolating the frequencies of different signals. First, the DC offset is removed from the signal in the pre-filter stage, and then the signals are amplified. They are then partitioned into 3 ranges and used to drive various LEDs. In addition to being cool, this device may have other applications, for example, it may be used as an indicator for loud noises to give visual alerts in noisy places or assist individuals with hearing impairment 

---
## Circuit Schematic
![Alt Text]({{ "/assets/LEDcircuit.png" | relative_url }})

---
## Built Circuit
![Alt Text]({{ "/assets/LEDbuiltcircuit.png" | relative_url }})


