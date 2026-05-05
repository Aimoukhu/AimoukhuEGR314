---
title: Appendix - Power Budget
---

## Overview
I took the main components of the Inertial Measurement Unit Subsystem and found the maximum current of the electrical components in the system. I then performed calculations to see if the power supply would be able to handle the components. A safety margin was included to account for any high current consumption, and a budget was put together. 

>The current power budget satisfies the requirements of the subsystem.


![budget1](AndrewPowerBudget.png){style width:"350" height:"300;"}

<!-- ![budget2](budgetPg2.png){style width:"350" height:"300;"}

![budget3](budgetPg3.png){style width:"350" height:"300;"} -->

## Conclusions

From the prepare Power Budget, I listed each major component (ESP32 and IMU) and summing their maximum current draw on the 3.3V rail. Then I added a safety margin to account for spikes , giving a total required current of about 1275 mA. This helped me verify that the selected regulator (2A max) and external supply can handle the load. The conclusion is that the system has sufficient power capacity with extra room for future expansion.

## Resouces

The power budget as a PDF download is available [*here*](AndrewPowerBudget.pdf), and a Microsoft Excel Sheet [*here*](AndrewPowerBudget.xlsx).