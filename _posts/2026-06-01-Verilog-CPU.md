---
layout: post
title: Verilog CPU
---
<p class="message">
  This is an active project! Tune in for updates 📢
</p>

## Motivation
I spent a long time trying to come up with a summer project that motivated me. It was challenging to come up with a challenging but doable project. 
I chose a Verilog-based project because of my interest in digital design. Digital Systems and Computer Systems have been some of my favorite college courses so far.
Learning a Hardware description language is a valuable skill and will be important for my next system in my FPGA course.
I am excited to dig deep into computer architecture. I will start at the gate level and build my way up module by module. My first milestone will be to complete an ALU.

---
## Getting Started
It took me a fair amount of time to get setup/comfterable. First, I finally installed WSL (Windows Subsystem for Linux), something I probably should have done years ago. 
Installing iVerilog and GTKWave was then quite easy. To get warmed up with Verilog, I started with the classic logic gates. The AND gate was my first.

```verilog
module and_gate(
    input a,
    input b,
    output y);
    assign y =a&b;
endmodule
```
Each module needs a test bench file to test it. Then I can visualize the result in GTKWave
![Alt Text]({{ "/assets/GTK_AND.png" | relative_url }})

