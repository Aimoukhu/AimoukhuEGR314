---
title: Reflection
---

## Review of Module's Success

Looking back at my module requirements, I was able to successfully accomplish several of the outlined goals. I integrated a 6-axis IMU sensor (accelerometer + gyroscope), implemented sensor fusion to output pitch and roll orientation data, and established UART serial communication for data transmission. The shared power rail and microcontroller requirements were met using an ESP32, and I was able to get I²C communication working with the IMU sensor.
The primary requirement I failed to meet was the on-board 3.3V switching power regulator which i had to brekout into through hole components rather than designing and populating a surface-mounted regulator circuit directly on my PCB. 

## Module Startup Tip

* Solder Component by Component and check connections at every step.
* Develop soft coding and debugging skill to help understand what you intend to code.

## Lessons Learned

* Careful when plugging in power to rails to avoid frying the board.
* Ensure the entire team is on the same page with communication protocols.
* Build in jumper points to test and jump you components incase of final minute hardware changes.
* Double check the datasheet and your schematic at all times, there is always a missing capacitor.
* Ensure you know the spacing and sizing of the footprints, don't just place them anywhere.
* Ensure you get email feedback on every submission. Don't just assume its done.
* Record each team test and compile the videos to display incase of misfortunes and during the innovation showcase demonstration.
* Get enough sleep and don't procrastinate any work.
* AI is very redundant in coding. Try your best to avoid or clean up the code.
* Connect all free pins to headers.


## Recommendations for Future Students

* Work quick and fast. All components should already be selected and known before purchase date. 
* Don't assume you'll find the components you need from the class or someone. Buy everything.
* Dont just trust AI to write code. I won't ask you to learn but if you're not good ask it to explain every line to you. Save the chats
* Do not procrastinate any team work. If you have to become the annoying person on the team, do it.
* Go to office hours early on in the semester and don't make others suffer because you now have problems with your design after making the pcb.
* Don't sweat the innovation showcase. Think of yourself as an attendee not the presenter.

