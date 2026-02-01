---
title: Module's Requirements
---

## Module Requirements
For this project, I am responsible for the IMU (Inertial Measurement Unit) sensor module. The IMU will be used to measure motion and orientation of the underwater rover. It provides information such as acceleration and rotation and is fundamental to any device that tracks how its moving in 3d space. This module will be used to help keep the vehicle stable and support navigation.

| **Requirement Description**                     | **Measure of<br> Threshold**         | **Target<br>Measure**                | **Stretch<br>Requirement<br>(Y-N)** |
|-------------------------------------------------|--------------------------------------|--------------------------------------|-------------------------------------|
| Surface mounted, 3.3V switching power regulator | 3.2 Volts                            | 3.3 Volts                            | No                                  |
| Surface mounted microcontroller                 | 1 PIC or ESP                         | 8-bit PIC                            | No                                  |
| Wireless Communication                          | Able to send or receive a Wi-Fi data | Send and receive Wi-Fi Data to MQTT  | Yes                                 |
| I2C Communication Interface                     | I²C communication                    | I²C with selectable address          | No                                  |
| Shared Power Rail                               | 3.2 volts                            | 3.3 volts                            | No                                  |
| Sample rate for sensor readings                 | 10 Hz                                | 50 Hz or higher                      | No                                  |
| Data transmission to MCU and HMI                | Serial UART at 9600 baud             | I2C AND wireless transmission        | No                                  |
| Calibration Capability                          | Manual one-time calibration          | Automatic calibration on startup     | Yes                                 |
| IMU Sensor                                      | 6-axis (accelerometer + gyroscope)   | 9-axis (accel + gyro + magnetometer) | Yes                                 |
| Orientation Accuracy                            | ±5 degrees for pitch/roll            | ±2 degrees for pitch/roll            | No                                  |
| Orientation Output                              | Raw sensor data output               | Sensor fusion (pitch, roll)          | No                                  |

