---
title: "All you need to know about TTP223 Capacitive Touch Sensor"
date: 2026-03-02T08:06:25+06:00
description: Complete theory and practical use of TTP223 Capacitive Touch Sensor
menu:
  sidebar:
    name: TTP223 Touch Sensor
    identifier: ttp223-touch
    weight: 20
tags: ["Basic", "Multi-lingual"]
categories: ["Basic"]
---

In this article, I'm going to discuss about TTP223 Capacitive Touch Sensor module.

A capacitive touch sensor detect touch by measuring variation in capacitance when a conductive object is brought closer to the sensor. 



Generally, in a capacitive touch sensor, copper pad on PCB act as bottom conductive plate, PCB material along with air act as dielectric and our finger act as the second plate. Therefore a capacitance is formed when our finger is brought closer to the copper pad.  TTP223 will detect this change in capacitance and provide an output. TTP223 can be configured for Active HIGH or Active LOW output. In both modes it suports both momentary and self latching output. However, every TTP223 module may not provide us the choice to configure. 

Here, I'm using this small red TTP223 capacitance touch module which provide us configuration choice. By default it comes in Active HIGH momentary output configuration. Inorder to configure the output, we have to short the necessary A or B pad to VCC (VCC pad is available near to both A and B).


<div>
  <img src="ModuleExplainer.svg"
       alt="TTP223 Module"
       style="display: block; margin: 0 auto; max-width: 600px; width: 100%; max-height: 400px;">
</div>

- If both A and B are left unconnected to the nearby VCC pad, which is the case by default, Output will be momentarily high when touched.
- If only A is connected to VCC, output will be low momentarily when touched and high otherwise.
- If only B is connected to VCC, output will be latched to high when touched. It will become low when touched again.

- If both A and B are connected to VCC, output will be latched to low when touched. It will be latched back to high when touched again. 
  
Here, i have connected B to VCC, which will act in self latching active high mode.
<div style="display: flex; 
            gap: 20px; 
            justify-content: center; 
            align-items: center;">

  <div style="width: 45%; height: 400px; 
              display: flex; 
              align-items: center; 
              justify-content: center;">
    <img src="LatchMode_TTP223.svg"
         alt="TTP223 in Latch Mode"
         style="max-width: 100%; max-height: 100%; object-fit: contain;">
  </div>

  <div style="width: 45%; height: 400px; 
              display: flex; 
              align-items: center; 
              justify-content: center;">
    <img src="TTP223_LatchingMode.gif"
         alt="Latching Mode working"
         style="max-width: 100%; max-height: 100%; object-fit: contain;">
  </div>

</div>
One thing to note is that, you don't actually need to touch  the sensor to turn it on. Capacitance will be formed at a small distance and hence produce the output as shown below.


<div>
  <img src="NotActuallyTouch.gif"
       alt="Not Actually Touch"
       style="display: block; margin: 0 auto; max-width: 600px; width: 100%; height: auto;">
</div>
If yo do not want false detecton or if you just want to reduce the sensitivity, you can add a capacitor (10pF or so) across the pad for sensitivity adjustment.


If you need to increase the sensitivity, you can add a conductor to the copper pad


<div style="display: flex; gap: 20px; justify-content: center;">
  <img src="TTP223_with_wire.jpeg" alt="TTP223 with wire for Increased sensitivity" width="45%">
  <img src="NotActuallyTouch_Far.gif" alt="Not Actually Touch Increased sensitivity" width="45%">
  
</div>




I hope you understood my blog. If any queries, feel free to reach out to me. Thank You!



# References
1. [Capacitive TTP223 Touch Sensors Explained with Arduino - Mario's Idea](https://www.youtube.com/watch?v=JuV29EQ96uQ)